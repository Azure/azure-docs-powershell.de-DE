---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 6937d79d6f60c053238075713f5d58432124e7e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936971"
---
# <span data-ttu-id="e2482-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="e2482-101">Get-AzIotHub</span></span>

## <span data-ttu-id="e2482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2482-102">SYNOPSIS</span></span>
<span data-ttu-id="e2482-103">Ruft Informationen zu den IotHubs in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e2482-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="e2482-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2482-104">SYNTAX</span></span>

### <span data-ttu-id="e2482-105">ListIotHubsByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="e2482-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2482-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="e2482-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2482-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2482-107">DESCRIPTION</span></span>
<span data-ttu-id="e2482-108">Ruft Informationen zu den IotHubs in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e2482-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="e2482-109">Sie können alle IotHub-Instanzen in einem Abonnement anzeigen oder Ihre Ergebnisse nach einer Ressourcengruppe oder einem bestimmten IotHub-Namen filtern.</span><span class="sxs-lookup"><span data-stu-id="e2482-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="e2482-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e2482-110">EXAMPLES</span></span>

### <span data-ttu-id="e2482-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e2482-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="e2482-112">Ruft alle IotHubs im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e2482-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="e2482-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e2482-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="e2482-114">Ruft alle IotHubs im Abonnement ab, die zur Ressourcengruppe "myresourcegroup" gehören.</span><span class="sxs-lookup"><span data-stu-id="e2482-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="e2482-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e2482-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="e2482-116">Ruft Informationen zum IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="e2482-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="e2482-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e2482-117">PARAMETERS</span></span>

### <span data-ttu-id="e2482-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2482-118">-DefaultProfile</span></span>
<span data-ttu-id="e2482-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e2482-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2482-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e2482-120">-Name</span></span>
<span data-ttu-id="e2482-121">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="e2482-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2482-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2482-122">-ResourceGroupName</span></span>
<span data-ttu-id="e2482-123">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e2482-123">Name of the ResourceGroup</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotHubsByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2482-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2482-124">CommonParameters</span></span>
<span data-ttu-id="e2482-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2482-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2482-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2482-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2482-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e2482-127">INPUTS</span></span>

### <span data-ttu-id="e2482-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e2482-128">System.String</span></span>

## <span data-ttu-id="e2482-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e2482-129">OUTPUTS</span></span>

### <span data-ttu-id="e2482-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e2482-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="e2482-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e2482-131">NOTES</span></span>

## <span data-ttu-id="e2482-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e2482-132">RELATED LINKS</span></span>
