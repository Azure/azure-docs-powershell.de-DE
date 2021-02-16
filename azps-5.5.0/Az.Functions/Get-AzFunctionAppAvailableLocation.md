---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappavailablelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
ms.openlocfilehash: 3ab2ab4778b7fdb12334db416c953a7c373c63b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175369"
---
# <span data-ttu-id="aa9a6-101">Get-AzFunctionAppAvailableLocation</span><span class="sxs-lookup"><span data-stu-id="aa9a6-101">Get-AzFunctionAppAvailableLocation</span></span>

## <span data-ttu-id="aa9a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa9a6-102">SYNOPSIS</span></span>
<span data-ttu-id="aa9a6-103">Ruft den Speicherort ab, an dem eine Funktions-App für das angegebene Betriebssystem und den Plantyp verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="aa9a6-103">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="aa9a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa9a6-104">SYNTAX</span></span>

```
Get-AzFunctionAppAvailableLocation [[-SubscriptionId] <String[]>] [[-PlanType] <String>] [[-OSType] <String>]
 [[-DefaultProfile] <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="aa9a6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa9a6-105">DESCRIPTION</span></span>
<span data-ttu-id="aa9a6-106">Ruft den Speicherort ab, an dem eine Funktions-App für das angegebene Betriebssystem und den Plantyp verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="aa9a6-106">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="aa9a6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aa9a6-107">EXAMPLES</span></span>

### <span data-ttu-id="aa9a6-108">Beispiel 1: Hier finden Sie die Speicherorte, an denen Premium für Windows verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="aa9a6-108">Example 1: Get the locations where Premium is available for Windows.</span></span> <span data-ttu-id="aa9a6-109">Wenn keine Parameter angegeben sind, wird "PlanType" auf "Premium" und "OSType" auf "Windows" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aa9a6-109">If no parameters are specified, PlanType is set to 'Premium' and OSType is set to 'Windows'.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
East Asia (Stage)
West India
South India
Canada Central
West US 2
UK West
UK South
East US 2 EUAP
Central US EUAP
Korea Central
France Central
Australia Central 2
Australia Central
Germany West Central
Norway East
```

<span data-ttu-id="aa9a6-110">Dieser Befehl ruft die Speicherorte ab, an denen Premium für Windows verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="aa9a6-110">This command gets the locations where Premium is available for Windows.</span></span>

### <span data-ttu-id="aa9a6-111">Beispiel 2: Hier finden Sie die Standorte, an denen Premium für Linux verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="aa9a6-111">Example 2: Get the locations where Premium is available for Linux.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation -PlanType Premium -OSType Linux

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
West India
Canada Central
West Central US
West US 2
UK West
UK South
Central US EUAP
Korea Central
France Central
Norway East
```

<span data-ttu-id="aa9a6-112">Dieser Befehl ruft die Speicherorte ab, an denen Premium für Linux verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="aa9a6-112">This command gets the locations where Premium is available for Linux.</span></span>

### <span data-ttu-id="aa9a6-113">Beispiel 3: Hier erhalten Sie die Standorte, an denen der Verbrauch für Windows verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="aa9a6-113">Example 3: Get the locations where Consumption is available for Windows.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation -PlanType Consumption -OSType Windows

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
East Asia (Stage)
Central India
West India
South India
Canada Central
Canada East
West Central US
West US 2
UK West
UK South
East US 2 EUAP
Central US EUAP
Korea Central
France Central
Australia Central 2
Australia Central
South Africa North
Switzerland North
Germany West Central
```

<span data-ttu-id="aa9a6-114">Dieser Befehl ruft die Speicherorte ab, an denen "Verbrauch" für Windows verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="aa9a6-114">This command gets the locations where Consumption is available for Windows.</span></span>

## <span data-ttu-id="aa9a6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa9a6-115">PARAMETERS</span></span>

### <span data-ttu-id="aa9a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa9a6-116">-DefaultProfile</span></span>
<span data-ttu-id="aa9a6-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa9a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa9a6-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="aa9a6-118">-OSType</span></span>
<span data-ttu-id="aa9a6-119">Der Betriebssystemtyp für den Serviceplan.</span><span class="sxs-lookup"><span data-stu-id="aa9a6-119">The OS type for the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa9a6-120">-PlanType</span><span class="sxs-lookup"><span data-stu-id="aa9a6-120">-PlanType</span></span>
<span data-ttu-id="aa9a6-121">Der Plantyp.</span><span class="sxs-lookup"><span data-stu-id="aa9a6-121">The plan type.</span></span>
<span data-ttu-id="aa9a6-122">Gültige Eingaben: Verbrauch oder Premium</span><span class="sxs-lookup"><span data-stu-id="aa9a6-122">Valid inputs: Consumption or Premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa9a6-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa9a6-123">-SubscriptionId</span></span>
<span data-ttu-id="aa9a6-124">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="aa9a6-124">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa9a6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa9a6-125">CommonParameters</span></span>
<span data-ttu-id="aa9a6-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa9a6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa9a6-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa9a6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa9a6-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aa9a6-128">INPUTS</span></span>

## <span data-ttu-id="aa9a6-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aa9a6-129">OUTPUTS</span></span>

### <span data-ttu-id="aa9a6-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span><span class="sxs-lookup"><span data-stu-id="aa9a6-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span></span>

## <span data-ttu-id="aa9a6-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aa9a6-131">NOTES</span></span>

<span data-ttu-id="aa9a6-132">ALIASE</span><span class="sxs-lookup"><span data-stu-id="aa9a6-132">ALIASES</span></span>

## <span data-ttu-id="aa9a6-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aa9a6-133">RELATED LINKS</span></span>

