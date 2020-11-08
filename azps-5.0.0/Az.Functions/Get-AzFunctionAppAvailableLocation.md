---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappavailablelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
ms.openlocfilehash: 3ab2ab4778b7fdb12334db416c953a7c373c63b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175636"
---
# <span data-ttu-id="fb981-101">Get-AzFunctionAppAvailableLocation</span><span class="sxs-lookup"><span data-stu-id="fb981-101">Get-AzFunctionAppAvailableLocation</span></span>

## <span data-ttu-id="fb981-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb981-102">SYNOPSIS</span></span>
<span data-ttu-id="fb981-103">Ruft die Position ab, an der eine Funktions-APP für das angegebene Betriebssystem und den Plantyp verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fb981-103">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="fb981-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb981-104">SYNTAX</span></span>

```
Get-AzFunctionAppAvailableLocation [[-SubscriptionId] <String[]>] [[-PlanType] <String>] [[-OSType] <String>]
 [[-DefaultProfile] <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="fb981-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb981-105">DESCRIPTION</span></span>
<span data-ttu-id="fb981-106">Ruft die Position ab, an der eine Funktions-APP für das angegebene Betriebssystem und den Plantyp verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fb981-106">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="fb981-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb981-107">EXAMPLES</span></span>

### <span data-ttu-id="fb981-108">Beispiel 1: Abrufen der Speicherorte, an denen Premium für Windows verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fb981-108">Example 1: Get the locations where Premium is available for Windows.</span></span> <span data-ttu-id="fb981-109">Wenn keine Parameter angegeben werden, wird "plantype" auf "Premium" festgelegt, und OSType ist auf "Windows" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fb981-109">If no parameters are specified, PlanType is set to 'Premium' and OSType is set to 'Windows'.</span></span>
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

<span data-ttu-id="fb981-110">Dieser Befehl ruft die Speicherorte ab, an denen Premium für Windows verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fb981-110">This command gets the locations where Premium is available for Windows.</span></span>

### <span data-ttu-id="fb981-111">Beispiel 2: Abrufen der Speicherorte, an denen Premium für Linux verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fb981-111">Example 2: Get the locations where Premium is available for Linux.</span></span>
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

<span data-ttu-id="fb981-112">Dieser Befehl ruft die Speicherorte ab, an denen Premium für Linux verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fb981-112">This command gets the locations where Premium is available for Linux.</span></span>

### <span data-ttu-id="fb981-113">Beispiel 3: Abrufen der Speicherorte, an denen der Verbrauch für Windows verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fb981-113">Example 3: Get the locations where Consumption is available for Windows.</span></span>
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

<span data-ttu-id="fb981-114">Dieser Befehl ruft die Speicherorte ab, an denen der Verbrauch für Windows verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fb981-114">This command gets the locations where Consumption is available for Windows.</span></span>

## <span data-ttu-id="fb981-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb981-115">PARAMETERS</span></span>

### <span data-ttu-id="fb981-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb981-116">-DefaultProfile</span></span>
<span data-ttu-id="fb981-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fb981-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb981-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="fb981-118">-OSType</span></span>
<span data-ttu-id="fb981-119">Der Typ des Betriebssystems für den Service Plan.</span><span class="sxs-lookup"><span data-stu-id="fb981-119">The OS type for the service plan.</span></span>

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

### <span data-ttu-id="fb981-120">-Plantype</span><span class="sxs-lookup"><span data-stu-id="fb981-120">-PlanType</span></span>
<span data-ttu-id="fb981-121">Der Plantyp.</span><span class="sxs-lookup"><span data-stu-id="fb981-121">The plan type.</span></span>
<span data-ttu-id="fb981-122">Gültige Eingaben: Verbrauch oder Prämie</span><span class="sxs-lookup"><span data-stu-id="fb981-122">Valid inputs: Consumption or Premium</span></span>

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

### <span data-ttu-id="fb981-123">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="fb981-123">-SubscriptionId</span></span>
<span data-ttu-id="fb981-124">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="fb981-124">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="fb981-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb981-125">CommonParameters</span></span>
<span data-ttu-id="fb981-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb981-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb981-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb981-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb981-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb981-128">INPUTS</span></span>

## <span data-ttu-id="fb981-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb981-129">OUTPUTS</span></span>

### <span data-ttu-id="fb981-130">Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. IGeoRegion</span><span class="sxs-lookup"><span data-stu-id="fb981-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span></span>

## <span data-ttu-id="fb981-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb981-131">NOTES</span></span>

<span data-ttu-id="fb981-132">Aliase</span><span class="sxs-lookup"><span data-stu-id="fb981-132">ALIASES</span></span>

## <span data-ttu-id="fb981-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb981-133">RELATED LINKS</span></span>

