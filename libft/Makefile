NAME = libft.a
OBJDIR = .obj

SRCS = ft_isdigit.c ft_memset.c ft_strjoin.c ft_strtrim.c ft_isprint.c\
ft_putchar_fd.c ft_strlcat.c ft_substr.c ft_atoi.c ft_itoa.c ft_putendl_fd.c\
ft_strlcpy.c ft_tolower.c ft_bzero.c ft_putnbr_fd.c ft_strlen.c\
ft_toupper.c ft_calloc.c ft_memchr.c ft_putstr_fd.c ft_strmapi.c ft_isalnum.c\
ft_memcmp.c ft_split.c ft_strncmp.c ft_isalpha.c ft_memcpy.c ft_strchr.c\
ft_strnstr.c ft_isascii.c ft_memmove.c ft_strdup.c ft_strrchr.c ft_striteri.c\

BONUS = ft_lstnew.c ft_lstadd_front.c ft_lstlast.c ft_lstsize.c ft_lstadd_back.c ft_lstdelone.c ft_lstclear.c ft_lstiter.c ft_lstmap.c ft_lstmap.c

OBJS = $(addprefix $(OBJDIR)/, $(SRCS:.c=.o))
OBJSBONUS = $(addprefix $(OBJDIR)/, $(BONUS:.c=.o))

CC		= gcc
RM		= rm -f

CFLAGS = -Wall -Wextra -Werror -g

# Colors
GREEN	= \033[1;32m
CYAN	= \033[1;36m
YELLOW	= \033[1;33m
RED		= \033[1;31m
RESET	= \033[0m

all:	${NAME}

$(OBJDIR)/%.o: %.c | $(OBJDIR)
		@$(CC) $(CFLAGS) -c $< -o $@
		@printf "$(CYAN)Compiling: $(RESET)%s\n" $<

$(OBJDIR):
		@mkdir -p $(OBJDIR)

$(NAME): ${OBJS}
		@ar rcs ${NAME} ${OBJS}
		@printf "$(GREEN)✔ $(NAME) compiled successfully!$(RESET)\n"

bonus:	${OBJS} ${OBJSBONUS}
		@ar rcs ${NAME} ${OBJS} ${OBJSBONUS}
		@printf "$(GREEN)✔ $(NAME) with bonus compiled successfully!$(RESET)\n"

clean:
		@${RM} -r ${OBJDIR}
		@printf "$(YELLOW)✔ Object files removed.$(RESET)\n"

fclean:	clean
		@${RM} ${NAME}
		@printf "$(RED)✔ $(NAME) removed.$(RESET)\n"

re:		fclean all

.PHONY: all clean fclean re bonus