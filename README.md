# url_to_dictonary
#This repository contains code make code from url to dict.



def getUrlDict(current_url):

    query = urlsplit(current_url).query

    params = parse_qs(query)

    dict(params)

    url_dict ={}

    for key,value in params.items():

        if key != '':

            url_dict.update({key: value[0] })

    return url_dict


current_url = request.get_full_path()

url_dict = getUrlDict(current_url)

element = url_dict['element']
