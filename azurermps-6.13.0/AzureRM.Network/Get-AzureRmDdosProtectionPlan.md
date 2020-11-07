---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azuredosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDdosProtectionPlan.md
ms.openlocfilehash: 2d1942dd5c069660d062922a069cc88b505748fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663649"
---
# <span data-ttu-id="b57f4-101">Get-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="b57f4-101">Get-AzureRmDdosProtectionPlan</span></span>

## <span data-ttu-id="b57f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b57f4-102">SYNOPSIS</span></span>
<span data-ttu-id="b57f4-103">Ruft einen DDoS-Schutzplan ab.</span><span class="sxs-lookup"><span data-stu-id="b57f4-103">Gets a DDoS protection plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b57f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b57f4-104">SYNTAX</span></span>

### <span data-ttu-id="b57f4-105">GetByNameAndGroup</span><span class="sxs-lookup"><span data-stu-id="b57f4-105">GetByNameAndGroup</span></span>
```
Get-AzureRmDdosProtectionPlan -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b57f4-106">Liste</span><span class="sxs-lookup"><span data-stu-id="b57f4-106">List</span></span>
```
Get-AzureRmDdosProtectionPlan [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b57f4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b57f4-107">DESCRIPTION</span></span>
<span data-ttu-id="b57f4-108">Das Get-AzureRmDdosProtectionPlan-Cmdlet erhält einen DDoS-Schutzplan.</span><span class="sxs-lookup"><span data-stu-id="b57f4-108">The Get-AzureRmDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="b57f4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b57f4-109">EXAMPLES</span></span>

### <span data-ttu-id="b57f4-110">Beispiel 1: Abrufen eines speziellen DDoS-Schutzplans</span><span class="sxs-lookup"><span data-stu-id="b57f4-110">Example 1: Get a specific DDoS protection plan</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="b57f4-111">In diesem Fall müssen wir sowohl **ResourceGroupName** -als auch **Name** -Attribute angeben, die der Ressourcengruppe und dem Namen des DDoS-Schutzplans entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b57f4-111">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="b57f4-112">Beispiel 2: Abrufen aller DDoS-schutzpläne in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b57f4-112">Example 2: Get all DDoS protection plans in a resource group</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="b57f4-113">In diesem Szenario geben wir nur den Parameter **ResourceGroupName** an, um eine Liste der DDoS-schutzpläne zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b57f4-113">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="b57f4-114">Beispiel 2: Abrufen aller DDoS-schutzpläne in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="b57f4-114">Example 2: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="b57f4-115">Hier geben wir keine Parameter an, um eine Liste aller DDoS-schutzpläne in einem Abonnement zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b57f4-115">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

## <span data-ttu-id="b57f4-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b57f4-116">PARAMETERS</span></span>

### <span data-ttu-id="b57f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b57f4-117">-DefaultProfile</span></span>
<span data-ttu-id="b57f4-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b57f4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b57f4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b57f4-119">-Name</span></span>
<span data-ttu-id="b57f4-120">Gibt den Namen des DDoS-Schutzplans an.</span><span class="sxs-lookup"><span data-stu-id="b57f4-120">Specifies the name of the DDoS protection plan.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndGroup
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b57f4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b57f4-121">-ResourceGroupName</span></span>
<span data-ttu-id="b57f4-122">Gibt den Namen der DDoS-Schutzplan-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b57f4-122">Specifies the name of the DDoS protection plan resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b57f4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b57f4-123">CommonParameters</span></span>
<span data-ttu-id="b57f4-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b57f4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b57f4-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b57f4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b57f4-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b57f4-126">INPUTS</span></span>

### <span data-ttu-id="b57f4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b57f4-127">System.String</span></span>

## <span data-ttu-id="b57f4-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b57f4-128">OUTPUTS</span></span>

### <span data-ttu-id="b57f4-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="b57f4-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="b57f4-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="b57f4-130">NOTES</span></span>

## <span data-ttu-id="b57f4-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b57f4-131">RELATED LINKS</span></span>

[<span data-ttu-id="b57f4-132">Neu – AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="b57f4-132">New-AzureRmDdosProtectionPlan</span></span>](./New-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="b57f4-133">Remove-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="b57f4-133">Remove-AzureRmDdosProtectionPlan</span></span>](./Remove-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="b57f4-134">Neu – AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b57f4-134">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="b57f4-135">Satz-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b57f4-135">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="b57f4-136">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b57f4-136">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)
