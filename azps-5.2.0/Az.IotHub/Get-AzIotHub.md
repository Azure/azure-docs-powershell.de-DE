---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 0656726757584bf923d6ecaa7642aa67ff46596a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302283"
---
# <span data-ttu-id="6776c-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="6776c-101">Get-AzIotHub</span></span>

## <span data-ttu-id="6776c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6776c-102">SYNOPSIS</span></span>
<span data-ttu-id="6776c-103">Ruft Informationen zu den IotHubs in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="6776c-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="6776c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6776c-104">SYNTAX</span></span>

### <span data-ttu-id="6776c-105">ListIotHubsByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="6776c-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6776c-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="6776c-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6776c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6776c-107">DESCRIPTION</span></span>
<span data-ttu-id="6776c-108">Ruft Informationen zu den IotHubs in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="6776c-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="6776c-109">Sie können alle Instanzen von IotHub in einem Abonnement anzeigen oder die Ergebnisse nach einer Ressourcengruppe oder einem bestimmten Namen für IotHub filtern.</span><span class="sxs-lookup"><span data-stu-id="6776c-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="6776c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6776c-110">EXAMPLES</span></span>

### <span data-ttu-id="6776c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6776c-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="6776c-112">Ruft alle IotHubs im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="6776c-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="6776c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6776c-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="6776c-114">Ruft alle IotHubs im Abonnement ab, die zur Ressourcengruppe "myresourcegroup" gehören.</span><span class="sxs-lookup"><span data-stu-id="6776c-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="6776c-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="6776c-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="6776c-116">Ruft Informationen zum IotHub namens "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="6776c-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="6776c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6776c-117">PARAMETERS</span></span>

### <span data-ttu-id="6776c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6776c-118">-DefaultProfile</span></span>
<span data-ttu-id="6776c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6776c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6776c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6776c-120">-Name</span></span>
<span data-ttu-id="6776c-121">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="6776c-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="6776c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6776c-122">-ResourceGroupName</span></span>
<span data-ttu-id="6776c-123">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6776c-123">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="6776c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6776c-124">CommonParameters</span></span>
<span data-ttu-id="6776c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6776c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6776c-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6776c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6776c-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6776c-127">INPUTS</span></span>

### <span data-ttu-id="6776c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6776c-128">System.String</span></span>

## <span data-ttu-id="6776c-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6776c-129">OUTPUTS</span></span>

### <span data-ttu-id="6776c-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6776c-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="6776c-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6776c-131">NOTES</span></span>

## <span data-ttu-id="6776c-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6776c-132">RELATED LINKS</span></span>
