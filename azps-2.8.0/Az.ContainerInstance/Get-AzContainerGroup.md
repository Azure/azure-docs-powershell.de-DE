---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
ms.openlocfilehash: 79f71c31f1a04b350733465338e9edcbd281af5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651846"
---
# <span data-ttu-id="a76b8-101">Get-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a76b8-101">Get-AzContainerGroup</span></span>

## <span data-ttu-id="a76b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a76b8-102">SYNOPSIS</span></span>
<span data-ttu-id="a76b8-103">Ruft Container Gruppen ab.</span><span class="sxs-lookup"><span data-stu-id="a76b8-103">Gets container groups.</span></span>

## <span data-ttu-id="a76b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a76b8-104">SYNTAX</span></span>

### <span data-ttu-id="a76b8-105">ListContainerGroupParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a76b8-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a76b8-106">GetContainerGroupInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="a76b8-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a76b8-107">GetContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="a76b8-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a76b8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a76b8-108">DESCRIPTION</span></span>
<span data-ttu-id="a76b8-109">Das Cmdlet " **Get-AzContainerGroup** " Ruft eine angegebene Containergruppe oder alle Container Gruppen in einer Ressourcengruppe oder dem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="a76b8-109">The **Get-AzContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="a76b8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a76b8-110">EXAMPLES</span></span>

### <span data-ttu-id="a76b8-111">Beispiel 1: Ruft eine angegebene Containergruppe ab.</span><span class="sxs-lookup"><span data-stu-id="a76b8-111">Example 1: Gets a specified container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer

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

<span data-ttu-id="a76b8-112">Der Befehl ruft die angegebene Containergruppe ab.</span><span class="sxs-lookup"><span data-stu-id="a76b8-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="a76b8-113">Beispiel 2: Ruft Container Gruppen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="a76b8-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="a76b8-114">Der Befehl ruft die Container Gruppen in der Ressourcengruppe ab `demo` .</span><span class="sxs-lookup"><span data-stu-id="a76b8-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="a76b8-115">Beispiel 3: Ruft Container Gruppen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="a76b8-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="a76b8-116">Der Befehl ruft die Container Gruppen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="a76b8-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="a76b8-117">Beispiel 4: Ruft Container Gruppen mithilfe der Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="a76b8-117">Example 4: Gets container groups using resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals demo -ResourceNameEquals mycontainer | Get-AzContainerGroup

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

<span data-ttu-id="a76b8-118">Der Befehl ruft die Containergruppe mit der Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="a76b8-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="a76b8-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="a76b8-119">PARAMETERS</span></span>

### <span data-ttu-id="a76b8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a76b8-120">-DefaultProfile</span></span>
<span data-ttu-id="a76b8-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a76b8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a76b8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a76b8-122">-Name</span></span>
<span data-ttu-id="a76b8-123">Der Name der Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="a76b8-123">The container group Name.</span></span>

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

### <span data-ttu-id="a76b8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a76b8-124">-ResourceGroupName</span></span>
<span data-ttu-id="a76b8-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a76b8-125">The resource Group Name.</span></span>

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

### <span data-ttu-id="a76b8-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a76b8-126">-ResourceId</span></span>
<span data-ttu-id="a76b8-127">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a76b8-127">The resource id.</span></span>

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

### <span data-ttu-id="a76b8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a76b8-128">CommonParameters</span></span>
<span data-ttu-id="a76b8-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a76b8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a76b8-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a76b8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a76b8-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a76b8-131">INPUTS</span></span>

### <span data-ttu-id="a76b8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a76b8-132">System.String</span></span>

## <span data-ttu-id="a76b8-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a76b8-133">OUTPUTS</span></span>

### <span data-ttu-id="a76b8-134">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a76b8-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="a76b8-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="a76b8-135">NOTES</span></span>

## <span data-ttu-id="a76b8-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a76b8-136">RELATED LINKS</span></span>
