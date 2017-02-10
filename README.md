# labeled_data
True label, abslute_height, height_difference, slope, roughness_1, roughness_2, vision_prediction, row, col

    base_path_geo_result = '/home/xi/workspace/labels/output/' + rosbag_name + '/' + rosbag_name + '_'
    for i in range(index_start, index_end):   
        file_path = base_path_geo_result + str(i) + '_features.txt'
        # print file_path
        with open(file_path) as f:
            content = f.readlines()
            for line in content:
                # print line
                features = line.split(' ')
                
                features_clean = []
                for feature in features:
                    feature = feature.replace('\n', '')
                    features_clean.append(float(feature))
