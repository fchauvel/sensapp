#
# SensApp
#
# Copyright (C) 2018 SINTEF Digital
# All rights reserved.
#
# This software may be modified and distributed under the terms
# of the MIT license.  See the LICENSE file for details.
#

FROM node:8.11.4-stretch


# Install the load-test engines
RUN npm install -g artillery
RUN artillery -V

# Copy the localfile
COPY ./test.yml /performance/test.yml
WORKDIR performance

# Run artillery
CMD ["artillery", "run", "test.yml"]
