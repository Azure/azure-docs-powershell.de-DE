---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/new-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
ms.openlocfilehash: 20daa8d14f77ca4563c072d58d1c2269235cb164
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470797"
---
# <span data-ttu-id="3b9bf-101">New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="3b9bf-101">New-AzContainerGroup</span></span>

## <span data-ttu-id="3b9bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b9bf-102">SYNOPSIS</span></span>
<span data-ttu-id="3b9bf-103">Erstellt eine Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-103">Creates a container group.</span></span>

## <span data-ttu-id="3b9bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b9bf-104">SYNTAX</span></span>

### <span data-ttu-id="3b9bf-105">CreateContainerGroupBaseParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3b9bf-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-AssignIdentity] [-OsType <String>]
 [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b9bf-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="3b9bf-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-AssignIdentity] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b9bf-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span><span class="sxs-lookup"><span data-stu-id="3b9bf-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b9bf-108">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b9bf-108">ExplicitIdentityParameterSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b9bf-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b9bf-109">DESCRIPTION</span></span>
<span data-ttu-id="3b9bf-110">Die **Cmdlets "New-AzContainerGroup"** erstellen eine Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-110">The **New-AzContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="3b9bf-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3b9bf-111">EXAMPLES</span></span>

### <span data-ttu-id="3b9bf-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3b9bf-112">Example 1</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="3b9bf-113">Mit diesen Befehlen wird eine Containergruppe mit dem neuesten nginx-Bild erstellt und eine öffentliche IP-Adresse mit Port 8000 geöffnet.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-113">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="3b9bf-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3b9bf-114">Example 2</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="3b9bf-115">Mit diesen Befehlen wird eine Containergruppe erstellt und ein benutzerdefiniertes Skript innerhalb des Containers ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-115">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="3b9bf-116">Beispiel 3: Erstellt eine Containergruppe für die Ausführung bis zum Abschluss.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-116">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="3b9bf-117">Mit diesen Befehlen wird eine Containergruppe erstellt, in der "Hallo" und Stopps gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-117">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="3b9bf-118">Beispiel 4: Erstellt eine Containergruppe mithilfe eines Bilds in der Azure Container Registry.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-118">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myacr}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="3b9bf-119">Mit diesen Befehlen wird eine Containergruppe mithilfe eines nginx-Bilds in der Azure Container Registry erstellt.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-119">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="3b9bf-120">Beispiel 5: Erstellt eine Containergruppe mithilfe eines Bilds in der benutzerdefinierten Containerbildregistrierung.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-120">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="3b9bf-121">Mit diesen Befehlen wird eine Containergruppe erstellt, indem ein benutzerdefiniertes Bild aus einer benutzerdefinierten Containerbildregistrierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-121">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="3b9bf-122">Beispiel 6: Erstellt eine Containergruppe, die das Azure -Dateivolume einbeigt.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-122">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name mycontainer -Image alpine -AzureFileVolumeShareName myshare -AzureFileVolumeAccountCredential $mycred -AzureFileVolumeMountPath /mnt/azfile

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  : {AzureFile}
State                    : Running
Events                   : {}
```

<span data-ttu-id="3b9bf-123">Mit diesen Befehlen wird eine Containergruppe erstellt, in der die bereitgestellte Azure-Dateifreigabe bereitgestellt `/mnt/azfile` wird.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-123">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

### <span data-ttu-id="3b9bf-124">Beispiel 7</span><span class="sxs-lookup"><span data-stu-id="3b9bf-124">Example 7</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -AssignIdentity

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="3b9bf-125">Mit diesen Befehlen wird eine Containergruppe mit einer vom System zugewiesenen Identität erstellt, die das neueste nginx-Bild verwendet, und es wird eine öffentliche IP-Adresse mit Öffnen von Port 8000 anfordert.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-125">This commands creates a container group with system assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="3b9bf-126">Beispiel 8</span><span class="sxs-lookup"><span data-stu-id="3b9bf-126">Example 8</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -IdentityType SystemAssignedUserAssigned -IdentityId /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<UserIdentityName>

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="3b9bf-127">Mit diesen Befehlen wird eine Containergruppe mit dem System zugewiesenen Identität und der vom Benutzer zugewiesenen Identität mithilfe des neuesten nginx-Bilds erstellt, und es wird eine öffentliche IP-Adresse mit Öffnen von Port 8000 anfordert.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-127">This commands creates a container group with system assigned and user assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

## <span data-ttu-id="3b9bf-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b9bf-128">PARAMETERS</span></span>

### <span data-ttu-id="3b9bf-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3b9bf-129">-AssignIdentity</span></span>
<span data-ttu-id="3b9bf-130">Aktivieren der vom System zugewiesenen Identität</span><span class="sxs-lookup"><span data-stu-id="3b9bf-130">Enable system assigned identity</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateContainerGroupBaseParamSet, CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-131">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3b9bf-131">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="3b9bf-132">Die Anmeldeinformationen für das Speicherkonto der Azure-Dateifreigabe, um bereitgestellt zu werden, wobei der Benutzername der Name des Speicherkontos und der Schlüssel der Speicherkontoschlüssel ist.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-132">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-133">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="3b9bf-133">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="3b9bf-134">Der Bereitstellungspfad für das Azure-Dateivolume.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-134">The mount path for the Azure File volume.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-135">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="3b9bf-135">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="3b9bf-136">Der Name der Azure-Dateifreigabe, die bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-136">The name of the Azure File share to mount.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-137">-Command</span><span class="sxs-lookup"><span data-stu-id="3b9bf-137">-Command</span></span>
<span data-ttu-id="3b9bf-138">Der Befehl, der im Container ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-138">The command to run in the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-139">-Cpu</span><span class="sxs-lookup"><span data-stu-id="3b9bf-139">-Cpu</span></span>
<span data-ttu-id="3b9bf-140">Die erforderlichen CPU-Kerne.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-140">The required CPU cores.</span></span>
<span data-ttu-id="3b9bf-141">Standard: 1</span><span class="sxs-lookup"><span data-stu-id="3b9bf-141">Default: 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b9bf-142">-DefaultProfile</span></span>
<span data-ttu-id="3b9bf-143">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-144">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="3b9bf-144">-DnsNameLabel</span></span>
<span data-ttu-id="3b9bf-145">Die Namenbezeichnung des DNS für die IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-145">The DNS name label for the IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-146">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="3b9bf-146">-EnvironmentVariable</span></span>
<span data-ttu-id="3b9bf-147">Die Containerumgebungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-147">The container environment variables.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-148">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="3b9bf-148">-IdentityId</span></span>
<span data-ttu-id="3b9bf-149">Dem Benutzer zugewiesene Identitäts-IDs</span><span class="sxs-lookup"><span data-stu-id="3b9bf-149">The user assigned identity IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-150">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="3b9bf-150">-IdentityType</span></span>
<span data-ttu-id="3b9bf-151">Der verwaltete Identitätstyp</span><span class="sxs-lookup"><span data-stu-id="3b9bf-151">The managed identity type</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerInstance.Models.ResourceIdentityType
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet, ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-152">-Image</span><span class="sxs-lookup"><span data-stu-id="3b9bf-152">-Image</span></span>
<span data-ttu-id="3b9bf-153">Das Containerbild.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-153">The container image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-154">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="3b9bf-154">-IpAddressType</span></span>
<span data-ttu-id="3b9bf-155">Der IP-Adresstyp.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-155">The IP address type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Public

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-156">-Location</span><span class="sxs-lookup"><span data-stu-id="3b9bf-156">-Location</span></span>
<span data-ttu-id="3b9bf-157">Die Containergruppe "Location".</span><span class="sxs-lookup"><span data-stu-id="3b9bf-157">The container group Location.</span></span>
<span data-ttu-id="3b9bf-158">Standard für den Speicherort der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-158">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-159">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="3b9bf-159">-MemoryInGB</span></span>
<span data-ttu-id="3b9bf-160">Der erforderliche Speicher in GB.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-160">The required memory in GB.</span></span>
<span data-ttu-id="3b9bf-161">Standard: 1,5</span><span class="sxs-lookup"><span data-stu-id="3b9bf-161">Default: 1.5</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases: Memory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-162">-Name</span><span class="sxs-lookup"><span data-stu-id="3b9bf-162">-Name</span></span>
<span data-ttu-id="3b9bf-163">Der Containergruppenname.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-163">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-164">-OsType</span><span class="sxs-lookup"><span data-stu-id="3b9bf-164">-OsType</span></span>
<span data-ttu-id="3b9bf-165">Der Containerbetriebssystemtyp.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-165">The container OS type.</span></span>
<span data-ttu-id="3b9bf-166">Standard: Linux</span><span class="sxs-lookup"><span data-stu-id="3b9bf-166">Default: Linux</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Linux, Windows

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-167">-Port</span><span class="sxs-lookup"><span data-stu-id="3b9bf-167">-Port</span></span>
<span data-ttu-id="3b9bf-168">Die zu öffnende(n) Port(n).</span><span class="sxs-lookup"><span data-stu-id="3b9bf-168">The port(s) to open.</span></span> <span data-ttu-id="3b9bf-169">Standard: [80]</span><span class="sxs-lookup"><span data-stu-id="3b9bf-169">Default: [80]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-170">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="3b9bf-170">-RegistryCredential</span></span>
<span data-ttu-id="3b9bf-171">Die Anmeldeinformationen für die benutzerdefinierte Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-171">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-172">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="3b9bf-172">-RegistryServerDomain</span></span>
<span data-ttu-id="3b9bf-173">Der Anmeldeserver der benutzerdefinierten Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-173">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b9bf-174">-ResourceGroupName</span></span>
<span data-ttu-id="3b9bf-175">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-175">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-176">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="3b9bf-176">-RestartPolicy</span></span>
<span data-ttu-id="3b9bf-177">Die Richtlinie für den Containerneustart.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-177">The container restart policy.</span></span> <span data-ttu-id="3b9bf-178">Standard: Immer</span><span class="sxs-lookup"><span data-stu-id="3b9bf-178">Default: Always</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Always, Never, OnFailure

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b9bf-179">-Tag</span></span>
<span data-ttu-id="3b9bf-180">{{Fill Tag Description}}</span><span class="sxs-lookup"><span data-stu-id="3b9bf-180">{{Fill Tag Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b9bf-181">-Confirm</span></span>
<span data-ttu-id="3b9bf-182">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-183">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3b9bf-183">-WhatIf</span></span>
<span data-ttu-id="3b9bf-184">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b9bf-185">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-185">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9bf-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b9bf-186">CommonParameters</span></span>
<span data-ttu-id="3b9bf-187">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b9bf-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b9bf-188">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b9bf-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b9bf-189">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3b9bf-189">INPUTS</span></span>

### <span data-ttu-id="3b9bf-190">System.String</span><span class="sxs-lookup"><span data-stu-id="3b9bf-190">System.String</span></span>

### <span data-ttu-id="3b9bf-191">System.String[]</span><span class="sxs-lookup"><span data-stu-id="3b9bf-191">System.String[]</span></span>

### <span data-ttu-id="3b9bf-192">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3b9bf-192">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3b9bf-193">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3b9bf-193">OUTPUTS</span></span>

### <span data-ttu-id="3b9bf-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="3b9bf-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="3b9bf-195">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3b9bf-195">NOTES</span></span>

## <span data-ttu-id="3b9bf-196">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3b9bf-196">RELATED LINKS</span></span>
