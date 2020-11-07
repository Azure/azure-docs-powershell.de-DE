---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
ms.openlocfilehash: 1f57a8a9cc65ab9ff4955d6d11e6f4c1a91c417e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822319"
---
# <span data-ttu-id="c0d1d-101">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c0d1d-101">Get-AzNetworkProfile</span></span>

## <span data-ttu-id="c0d1d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c0d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="c0d1d-103">Ruft eine vorhandene Netzwerkprofil-Ressource auf oberster Ebene ab</span><span class="sxs-lookup"><span data-stu-id="c0d1d-103">Gets an existing network profile top level resource</span></span>

## <span data-ttu-id="c0d1d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0d1d-104">SYNTAX</span></span>

### <span data-ttu-id="c0d1d-105">GetByResourceNameNoExpandParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c0d1d-105">GetByResourceNameNoExpandParameterSet (Default)</span></span>
```
Get-AzNetworkProfile [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0d1d-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0d1d-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0d1d-107">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0d1d-107">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0d1d-108">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0d1d-108">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0d1d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0d1d-109">DESCRIPTION</span></span>
<span data-ttu-id="c0d1d-110">Das Cmdlet " **Get-AzNetworkProfile** " Ruft eine vorhandene Netzwerkprofil Ressource auf oberster Ebene ab</span><span class="sxs-lookup"><span data-stu-id="c0d1d-110">The **Get-AzNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="c0d1d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0d1d-111">EXAMPLES</span></span>

### <span data-ttu-id="c0d1d-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c0d1d-112">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1
```

<span data-ttu-id="c0d1d-113">Dadurch wird das Netzwerkprofil-Np1 in der Ressourcengruppe abgerufen RG1</span><span class="sxs-lookup"><span data-stu-id="c0d1d-113">This retrieves the network profile np1 in resource group rg1</span></span>

### <span data-ttu-id="c0d1d-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c0d1d-114">Example 2</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np*

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np2
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np2
```

<span data-ttu-id="c0d1d-115">Damit werden die Netzwerkprofile abgerufen, die mit "NP" beginnen.</span><span class="sxs-lookup"><span data-stu-id="c0d1d-115">This retrieves the network profiles that start with "np"</span></span>

## <span data-ttu-id="c0d1d-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0d1d-116">PARAMETERS</span></span>

### <span data-ttu-id="c0d1d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0d1d-117">-DefaultProfile</span></span>
<span data-ttu-id="c0d1d-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c0d1d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0d1d-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="c0d1d-119">-ExpandResource</span></span>
<span data-ttu-id="c0d1d-120">Der Ressourcenverweis, der erweitert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c0d1d-120">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceIdExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d1d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c0d1d-121">-Name</span></span>
<span data-ttu-id="c0d1d-122">Der Name des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="c0d1d-122">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c0d1d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0d1d-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0d1d-124">Der Ressourcengruppenname des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="c0d1d-124">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c0d1d-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c0d1d-125">-ResourceId</span></span>
<span data-ttu-id="c0d1d-126">Die Azure Resource Manager-ID des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="c0d1d-126">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d1d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0d1d-127">CommonParameters</span></span>
<span data-ttu-id="c0d1d-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0d1d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0d1d-129">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0d1d-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0d1d-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c0d1d-130">INPUTS</span></span>

### <span data-ttu-id="c0d1d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c0d1d-131">System.String</span></span>

## <span data-ttu-id="c0d1d-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c0d1d-132">OUTPUTS</span></span>

### <span data-ttu-id="c0d1d-133">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c0d1d-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="c0d1d-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="c0d1d-134">NOTES</span></span>

## <span data-ttu-id="c0d1d-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c0d1d-135">RELATED LINKS</span></span>

[<span data-ttu-id="c0d1d-136">Neu – AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c0d1d-136">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="c0d1d-137">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c0d1d-137">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="c0d1d-138">Satz-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c0d1d-138">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
