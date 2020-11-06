---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/get-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
ms.openlocfilehash: b2107a667fe3d00ec0b6e9180b2edc99e864445c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476173"
---
# <span data-ttu-id="b5924-101">Get-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="b5924-101">Get-AzureRmContainerGroup</span></span>

## <span data-ttu-id="b5924-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b5924-102">SYNOPSIS</span></span>
<span data-ttu-id="b5924-103">Ruft Container Gruppen ab.</span><span class="sxs-lookup"><span data-stu-id="b5924-103">Gets container groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5924-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5924-104">SYNTAX</span></span>

### <span data-ttu-id="b5924-105">ListContainerGroupParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b5924-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzureRmContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5924-106">GetContainerGroupInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="b5924-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5924-107">GetContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="b5924-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzureRmContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5924-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b5924-108">DESCRIPTION</span></span>
<span data-ttu-id="b5924-109">Das Cmdlet " **Get-AzureRmContainerGroup** " Ruft eine angegebene Containergruppe oder alle Container Gruppen in einer Ressourcengruppe oder dem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b5924-109">The **Get-AzureRmContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="b5924-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b5924-110">EXAMPLES</span></span>

### <span data-ttu-id="b5924-111">Beispiel 1: Ruft eine angegebene Containergruppe ab.</span><span class="sxs-lookup"><span data-stu-id="b5924-111">Example 1: Gets a specified container group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
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

<span data-ttu-id="b5924-112">Der Befehl ruft die angegebene Containergruppe ab.</span><span class="sxs-lookup"><span data-stu-id="b5924-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="b5924-113">Beispiel 2: Ruft Container Gruppen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="b5924-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="b5924-114">Der Befehl ruft die Container Gruppen in der Ressourcengruppe ab `demo` .</span><span class="sxs-lookup"><span data-stu-id="b5924-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="b5924-115">Beispiel 3: Ruft Container Gruppen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b5924-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzureRmContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="b5924-116">Der Befehl ruft die Container Gruppen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b5924-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="b5924-117">Beispiel 4: Ruft Container Gruppen mithilfe der Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="b5924-117">Example 4: Gets container groups using resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals demo -ResourceNameEquals mycontainer | Get-AzureRmContainerGroup

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
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

<span data-ttu-id="b5924-118">Der Befehl ruft die Containergruppe mit der Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="b5924-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="b5924-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5924-119">PARAMETERS</span></span>

### <span data-ttu-id="b5924-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5924-120">-DefaultProfile</span></span>
<span data-ttu-id="b5924-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b5924-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5924-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b5924-122">-Name</span></span>
<span data-ttu-id="b5924-123">Der Name der Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="b5924-123">The container group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5924-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5924-124">-ResourceGroupName</span></span>
<span data-ttu-id="b5924-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b5924-125">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListContainerGroupParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5924-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b5924-126">-ResourceId</span></span>
<span data-ttu-id="b5924-127">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b5924-127">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5924-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5924-128">CommonParameters</span></span>
<span data-ttu-id="b5924-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5924-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5924-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5924-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5924-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b5924-131">INPUTS</span></span>

### <span data-ttu-id="b5924-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b5924-132">System.String</span></span>

## <span data-ttu-id="b5924-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b5924-133">OUTPUTS</span></span>

### <span data-ttu-id="b5924-134">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="b5924-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="b5924-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="b5924-135">NOTES</span></span>

## <span data-ttu-id="b5924-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b5924-136">RELATED LINKS</span></span>
