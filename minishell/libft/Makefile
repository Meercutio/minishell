NAME		= libft.a
CC			= gcc -MD
FLAGS		= -Wall -Wextra -Werror
INC			= ./inc/libft.h
SRCS		= ft_atoi.c ft_bzero.c	\
	ft_calloc.c ft_putendl_fd.c		\
	ft_itoa.c ft_putchar_fd.c		\
	ft_putstr_fd.c ft_memccpy.c		\
	ft_memchr.c ft_memcmp.c			\
	ft_memcpy.c ft_isalnum.c		\
	ft_isalpha.c ft_isascii.c		\
	ft_isdigit.c ft_isprint.c		\
	ft_memmove.c ft_memset.c		\
	ft_split.c ft_strchr.c			\
	ft_strdup.c ft_strjoin.c		\
	ft_strlcat.c ft_strlcpy.c		\
	ft_strlen.c ft_strmapi.c		\
	ft_strncmp.c ft_strnstr.c		\
	ft_strrchr.c ft_strtrim.c		\
	ft_substr.c ft_tolower.c		\
	ft_toupper.c ft_putnbr_fd.c \
	ft_lstadd_back.c	\
	ft_lstadd_front.c	\
	ft_lstclear.c	\
	ft_lstdelone.c	\
	ft_lstiter.c	\
	ft_lstlast.c	\
	ft_lstsize.c	\
	ft_lstnew.c	\
	ft_lstmap.c	\
	ft_lstget_at.c \
	ft_putnbr_base_fd.c ft_putstrn_fd.c		\
	ft_putnchar_fd.c ft_isspace.c ft_uitoa.c	\
	ft_nbrlen.c ft_strrncmp.c ft_countchar.c	\
	ft_strenlarge.c ft_recursive_power.c		\
	ft_chartostr.c ft_sqrt.c ft_newvector.c		\
	ft_euclideandistance.c  ft_atoi2.c			\
	ft_free_matrix.c ft_dup_matrix.c			\
	ft_strchr_i.c ft_putmatrix_fd.c				\
	ft_matrixlen.c ft_strchars_i.c				\
	ft_between_chars.c ft_subsplit.c			\
	ft_extend_matrix.c ft_matrixtolst.c			\
 	ft_lsttomatrix.c ft_matrix_replace_in.c

OBJ_NAME	= $(SRCS:.c=.o)
OBJ			= $(addprefix $(OBJ_DIR),$(OBJ_NAME))
SRC_DIR 	= src/
OBJ_DIR 	= obj/
LIBC		= ar rcs
RM			= rm -f

all:		$(NAME)

$(NAME):	$(OBJ) $(INC)
	$(LIBC) ${NAME} ${OBJ}

$(OBJ_DIR)%.o:	$(SRC_DIR)%.c
	mkdir -p $(OBJ_DIR)
	$(CC) $(FLAGS) -o $@ -c $< -I $(INC)
clean:
	$(RM) $(OBJ)

fclean:		clean
	$(RM) $(NAME)

re:			fclean all

.PHONY:		all clean fclean re