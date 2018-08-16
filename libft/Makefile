# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: agoulas <marvin@42.fr>                     +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2017/11/08 15:28:36 by agoulas           #+#    #+#              #
#    Updated: 2018/01/22 14:35:34 by agoulas          ###   ########.fr        #
#                                                                              #
# **************************************************************************** #
NAME = libft.a
CFLAGS = -Wall -Werror -Wextra
SRC = srcs
OBJ = object

SOURCES = ft_atoi.c ft_isalnum.c ft_isascii.c ft_isprint.c \
		ft_memccpy.c ft_memcmp.c ft_memdel.c ft_memset.c \
		ft_putnbr.c ft_strcat.c ft_strclr.c ft_strcpy.c ft_strdup.c\
		ft_striter.c ft_strjoin.c ft_strlen.c ft_strmapi.c\
		ft_strncmp.c ft_strnequ.c ft_strrchr.c ft_strstr.c\
		ft_strtrim.c ft_tolower.c ft_bzero.c ft_isalpha.c\
		ft_isdigit.c ft_memalloc.c ft_memchr.c ft_memcpy.c\
		ft_memmove.c ft_putchar.c ft_putstr.c ft_strchr.c\
		ft_strcmp.c ft_strdel.c ft_strequ.c ft_striteri.c\
		ft_strlcat.c ft_strmap.c ft_strncat.c ft_strncpy.c ft_strnew.c\
		ft_strrev.c ft_strsub.c ft_toupper.c ft_strsplit.c\
		ft_itoa.c ft_putchar_fd.c ft_putstr_fd.c ft_strnstr.c\
		ft_putendl_fd.c ft_putnbr_fd.c ft_putendl.c \
		ft_lstnew.c ft_lstadd.c ft_lstdel.c ft_lstdelone.c ft_lstiter.c\
		ft_lstmap.c ft_isupper.c ft_islower.c ft_isspace.c ft_abs.c ft_pow.c\
		ft_is_prime.c ft_lstadd_last.c ft_lst_del_one.c ft_realloc.c\

SRCS=$(addprefix srcs/, $(SOURCES))
OBJS=$(addprefix build/, $(SOURCES:.c=.o))
HDR = includes

.PHONY: all clean fclean re

all: $(NAME)

$(NAME): $(OBJS)
	ar rc $(NAME) $(OBJS)
	ranlib $(NAME)
	@echo "Creating libft.a"

build:
	@mkdir build/

build/%.o: srcs/%.c | build
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	@rm -f $(OBJS)
	@rm -Rf build/
	@echo "delete file.o"

fclean: clean
	@rm -f $(NAME)
	@echo "start-up conditions"

re: fclean all 
	@echo "RE start-up"
