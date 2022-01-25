NAME	= minishell
CFLAGS	= -Wall -Wextra -Werror -MMD
RM		= rm -f
CC		= gcc
SRC_DIR	= src
OBJ_DIR	= obj
LIB_DIR	= libft/
LIBFT	= libft/libft.a
AR		= ar rcs

SRC = main.c builtins.c ft_strtrim_all.c exec.c	\
	fill_node.c get_params.c ft_cmdtrim.c	\
	expand.c heredoc.c error.c env.c custom_cmd.c	\
	get_next_line.c get_next_line_utils.c prompt.c	\
	ft_cmdsubsplit.c signal.c parse_args.c get_cmd.c

OBJ = $(addprefix $(OBJ_DIR)/, $(SRC:.c=.o))

all: $(NAME)

$(NAME): $(OBJ) $(LIBFT)
	$(CC) -L ~/.brew/opt/readline/lib -I ~/.brew/opt/readline/include $(CFLAGS) $(OBJ) -L./libft -lft -lreadline -o $@

$(LIBFT):
	make -C $(LIB_DIR)

$(OBJ_DIR)/%.o: $(SRC_DIR)/%.c
	mkdir -p $(OBJ_DIR)
	$(CC) -I ~/.brew/opt/readline/include $(CFLAGS) -c $< -o $@ -I ./libft/inc -I ./inc

clean:
	make -C $(LIB_DIR) clean
	$(RM) -r $(OBJ_DIR)

fclean: clean
	make -C $(LIB_DIR) fclean
	$(RM) $(NAME)

re: fclean all

-include $(OBJ_DIR)/*.d

.PHONY: all clean fclean re