# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: heddahbi <heddahbi@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2023/11/05 02:44:37 by abel-hid          #+#    #+#              #
#    Updated: 2023/12/13 21:31:28 by heddahbi         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #


NAME = cub3D

SRCS =	main.c\
		main_utils.c\
		$(wildcard parsing/*.c)\
		$(wildcard rendering/*.c)\
		$(wildcard raycasting/*.c)\
		
	

OBJS = $(SRCS:.c=.o)

CC = cc
RM = rm -f
CFLAGS = -Wall -Werror -Wextra 

all: $(NAME)

$(NAME):$(OBJS) ./includes/cub3D.h
	$(CC) $(OBJS) ../MLX42/build/libmlx42.a -Iinclude -lglfw -L"/Users/$(USER)/.brew/opt/glfw/lib/"  -o $(NAME) 
%.o: %.c ./includes/cub3D.h
	$(CC) $(CFLAGS) -Imlx -c $< -o $@

clean:
	$(RM) $(OBJS)

fclean: clean
	$(RM) $(NAME)

re: fclean all