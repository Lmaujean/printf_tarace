# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lmaujean <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2021/03/22 13:36:18 by lmaujean          #+#    #+#              #
#    Updated: 2021/04/14 11:28:50 by lmaujean         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME	= libft.a
SRCS	= ft_atoi.c ft_strlen.c ft_bzero.c \
		  ft_isalpha.c ft_isdigit.c ft_isalnum.c \
		  ft_isascii.c ft_isprint.c ft_strncmp.c \
		  ft_toupper.c ft_tolower.c ft_memset.c \
		  ft_memcpy.c ft_memchr.c ft_memccpy.c \
		  ft_memcmp.c ft_memmove.c ft_strchr.c \
		  ft_strrchr.c ft_strlcpy.c ft_strlcat.c \
		  ft_strnstr.c ft_strdup.c ft_calloc.c \
		  ft_putchar_fd.c ft_putstr_fd.c ft_putendl_fd.c \
		  ft_putnbr_fd.c ft_strjoin.c ft_strcpy.c \
		  ft_substr.c ft_split.c ft_strtrim.c	\
		  ft_strmapi.c ft_itoa.c

BONUS	= ft_lstnew.c ft_lstadd_front.c ft_lstsize.c \
		  ft_lstlast.c ft_lstadd_back.c ft_lstdelone.c \
		  ft_lstclear.c ft_lstiter.c ft_lstmap.c \


OBJS	= ${SRCS:.c=.o}
BOBJ	= ${BONUS:.c=.o}
HEADER  = libft.h

CC		= gcc
CFLAGS  = -Wall -Wextra -Werror
RM		= rm -f

$(NAME):	${OBJS}
			ar -rcs ${NAME} ${OBJS}

%.o: %.c
			${CC} -c ${CFLAGS} -o $@ $< -I ${HEADER}

all:		${NAME}

clean:
			${RM} ${OBJS} ${BOBJ}

fclean:		clean
			${RM} ${NAME}

re:			fclean all

.PHONY: $(NAME) all clean fclean re bonus

bonus:	$(OBJ) $(BOBJ)
		ar -rcs $(NAME) $(NAME) $(BOBJ)
