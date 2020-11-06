---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 63c54c5f1bb17af82e353b70e757bf91b1208958
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501921"
---
# <span data-ttu-id="ce99c-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="ce99c-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="ce99c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ce99c-102">SYNOPSIS</span></span>
<span data-ttu-id="ce99c-103">Erstellt eine Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="ce99c-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce99c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce99c-104">SYNTAX</span></span>

### <span data-ttu-id="ce99c-105">CreateContainerGroupBaseParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ce99c-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> -Image <String> [-Location <String>]
 [-OsType <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-Port <Int32>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce99c-106">CreateContainerGroupWithRegistryParamSet</span><span class="sxs-lookup"><span data-stu-id="ce99c-106">CreateContainerGroupWithRegistryParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> -Image <String> [-Location <String>]
 [-OsType <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-Port <Int32>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>]
 -RegistryCredential <PSCredential> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce99c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce99c-107">DESCRIPTION</span></span>
<span data-ttu-id="ce99c-108">Mit den Cmdlets **New-AzureRmContainerGroup** wird eine Containergruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="ce99c-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="ce99c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce99c-109">EXAMPLES</span></span>

### <span data-ttu-id="ce99c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ce99c-110">Example 1</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port 8000

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
```

<span data-ttu-id="ce99c-111">Mit diesen Befehlen wird eine Containergruppe mit dem neuesten nginx-Bild erstellt und eine öffentliche IP-Adresse mit dem Öffnen von Port 8000 angefordert.</span><span class="sxs-lookup"><span data-stu-id="ce99c-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="ce99c-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ce99c-112">Example 2</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

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
```

<span data-ttu-id="ce99c-113">Mit diesen Befehlen wird eine Containergruppe erstellt und ein benutzerdefiniertes Skript im Container ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce99c-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="ce99c-114">Beispiel 3: erstellt eine Containergruppe mithilfe von Bild in der Azure-Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="ce99c-114">Example 3: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

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
```

<span data-ttu-id="ce99c-115">Mit diesen Befehlen wird eine Containergruppe mit einem nginx-Bild in der Azure-Container Registrierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="ce99c-115">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="ce99c-116">Beispiel 4: Erstellen einer Containergruppe mithilfe von Bild in der benutzerdefinierten Container Bildregistrierung</span><span class="sxs-lookup"><span data-stu-id="ce99c-116">Example 4: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

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
```

<span data-ttu-id="ce99c-117">Mit diesen Befehlen wird eine Containergruppe mithilfe eines benutzerdefinierten Bilds aus einer benutzerdefinierten Container Bildregistrierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="ce99c-117">This commands creates a container group using a custom image from a custom container image registry.</span></span>

## <span data-ttu-id="ce99c-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce99c-118">PARAMETERS</span></span>

### <span data-ttu-id="ce99c-119">-Befehl</span><span class="sxs-lookup"><span data-stu-id="ce99c-119">-Command</span></span>
<span data-ttu-id="ce99c-120">Der Befehl, der im Container ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce99c-120">The command to run in the container.</span></span>

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

### <span data-ttu-id="ce99c-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ce99c-121">-Confirm</span></span>
<span data-ttu-id="ce99c-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce99c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce99c-123">-CPU</span><span class="sxs-lookup"><span data-stu-id="ce99c-123">-Cpu</span></span>
<span data-ttu-id="ce99c-124">Die erforderlichen CPU-Kerne.</span><span class="sxs-lookup"><span data-stu-id="ce99c-124">The required CPU cores.</span></span>
<span data-ttu-id="ce99c-125">Standard: 1</span><span class="sxs-lookup"><span data-stu-id="ce99c-125">Default: 1</span></span>

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

### <span data-ttu-id="ce99c-126">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="ce99c-126">-EnvironmentVariable</span></span>
<span data-ttu-id="ce99c-127">Die Container Umgebungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="ce99c-127">The container environment variables.</span></span>

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

### <span data-ttu-id="ce99c-128">-Bild</span><span class="sxs-lookup"><span data-stu-id="ce99c-128">-Image</span></span>
<span data-ttu-id="ce99c-129">Das Container Bild.</span><span class="sxs-lookup"><span data-stu-id="ce99c-129">The container image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce99c-130">-Ipaddresstype</span><span class="sxs-lookup"><span data-stu-id="ce99c-130">-IpAddressType</span></span>
<span data-ttu-id="ce99c-131">Der Typ der IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="ce99c-131">The IP address type.</span></span>

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

### <span data-ttu-id="ce99c-132">-Standort</span><span class="sxs-lookup"><span data-stu-id="ce99c-132">-Location</span></span>
<span data-ttu-id="ce99c-133">Der Speicherort der Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="ce99c-133">The container group Location.</span></span>
<span data-ttu-id="ce99c-134">Standardmäßig wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce99c-134">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="ce99c-135">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="ce99c-135">-MemoryInGB</span></span>
<span data-ttu-id="ce99c-136">Der erforderliche Arbeitsspeicher in GB.</span><span class="sxs-lookup"><span data-stu-id="ce99c-136">The required memory in GB.</span></span>
<span data-ttu-id="ce99c-137">Standard: 1,5</span><span class="sxs-lookup"><span data-stu-id="ce99c-137">Default: 1.5</span></span>

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

### <span data-ttu-id="ce99c-138">-Name</span><span class="sxs-lookup"><span data-stu-id="ce99c-138">-Name</span></span>
<span data-ttu-id="ce99c-139">Der Name der Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="ce99c-139">The container group name.</span></span>

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

### <span data-ttu-id="ce99c-140">-OsType</span><span class="sxs-lookup"><span data-stu-id="ce99c-140">-OsType</span></span>
<span data-ttu-id="ce99c-141">Der Typ des Container-Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="ce99c-141">The container OS type.</span></span>
<span data-ttu-id="ce99c-142">Standard: Linux</span><span class="sxs-lookup"><span data-stu-id="ce99c-142">Default: Linux</span></span>

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

### <span data-ttu-id="ce99c-143">-Port</span><span class="sxs-lookup"><span data-stu-id="ce99c-143">-Port</span></span>
<span data-ttu-id="ce99c-144">Der zu öffnende Port.</span><span class="sxs-lookup"><span data-stu-id="ce99c-144">The port to open.</span></span>
<span data-ttu-id="ce99c-145">Standard: 80</span><span class="sxs-lookup"><span data-stu-id="ce99c-145">Default: 80</span></span>

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

### <span data-ttu-id="ce99c-146">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="ce99c-146">-RegistryCredential</span></span>
<span data-ttu-id="ce99c-147">Die Anmeldeinformationen für benutzerdefinierte Container-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="ce99c-147">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithRegistryParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce99c-148">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="ce99c-148">-RegistryServerDomain</span></span>
<span data-ttu-id="ce99c-149">Der benutzerdefinierte Container Registrierungs Anmeldeserver.</span><span class="sxs-lookup"><span data-stu-id="ce99c-149">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithRegistryParamSet
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce99c-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce99c-150">-ResourceGroupName</span></span>
<span data-ttu-id="ce99c-151">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ce99c-151">The resource group name.</span></span>

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

### <span data-ttu-id="ce99c-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="ce99c-152">-Tag</span></span>
<span data-ttu-id="ce99c-153">{{Fill Tag Description}}</span><span class="sxs-lookup"><span data-stu-id="ce99c-153">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="ce99c-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce99c-154">-WhatIf</span></span>
<span data-ttu-id="ce99c-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce99c-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce99c-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce99c-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce99c-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce99c-157">-DefaultProfile</span></span>
<span data-ttu-id="ce99c-158">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ce99c-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce99c-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce99c-159">CommonParameters</span></span>
<span data-ttu-id="ce99c-160">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce99c-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce99c-161">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce99c-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce99c-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ce99c-162">INPUTS</span></span>

### <span data-ttu-id="ce99c-163">System. String</span><span class="sxs-lookup"><span data-stu-id="ce99c-163">System.String</span></span>
<span data-ttu-id="ce99c-164">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ce99c-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ce99c-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ce99c-165">OUTPUTS</span></span>

### <span data-ttu-id="ce99c-166">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="ce99c-166">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="ce99c-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce99c-167">NOTES</span></span>

## <span data-ttu-id="ce99c-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ce99c-168">RELATED LINKS</span></span>

