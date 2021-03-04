---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: bbe4cf87c3af86cd8a4e72f239d4aca7c3386786
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933296"
---
# <span data-ttu-id="2e6bd-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2e6bd-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="2e6bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e6bd-102">SYNOPSIS</span></span>
<span data-ttu-id="2e6bd-103">Ruft einen Azure App Service-Plan in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="2e6bd-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="2e6bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e6bd-104">SYNTAX</span></span>

### <span data-ttu-id="2e6bd-105">S1</span><span class="sxs-lookup"><span data-stu-id="2e6bd-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e6bd-106">S2</span><span class="sxs-lookup"><span data-stu-id="2e6bd-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e6bd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2e6bd-107">DESCRIPTION</span></span>
<span data-ttu-id="2e6bd-108">Das **Get-AzAppServicePlan-Cmdlet** ruft einen Azure App Service-Plan in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="2e6bd-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="2e6bd-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2e6bd-109">EXAMPLES</span></span>

### <span data-ttu-id="2e6bd-110">Beispiel 1: Herunterladen eines App Service-Plans aus einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2e6bd-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="2e6bd-111">Dieser Befehl ruft den App Service-Plan namens ContosoASP ab, der zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="2e6bd-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="2e6bd-112">Beispiel 2: Herunterladen aller App Service-Pläne an einem Speicherort</span><span class="sxs-lookup"><span data-stu-id="2e6bd-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="2e6bd-113">Dieser Befehl ruft alle App Service-Pläne ab, die sich in der Region "Usa, Westen" befinden.</span><span class="sxs-lookup"><span data-stu-id="2e6bd-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="2e6bd-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2e6bd-114">PARAMETERS</span></span>

### <span data-ttu-id="2e6bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e6bd-115">-DefaultProfile</span></span>
<span data-ttu-id="2e6bd-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2e6bd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e6bd-117">-Location</span><span class="sxs-lookup"><span data-stu-id="2e6bd-117">-Location</span></span>
<span data-ttu-id="2e6bd-118">Ort</span><span class="sxs-lookup"><span data-stu-id="2e6bd-118">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e6bd-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2e6bd-119">-Name</span></span>
<span data-ttu-id="2e6bd-120">Name des App-Dienstplans</span><span class="sxs-lookup"><span data-stu-id="2e6bd-120">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e6bd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e6bd-121">-ResourceGroupName</span></span>
<span data-ttu-id="2e6bd-122">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="2e6bd-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e6bd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e6bd-123">CommonParameters</span></span>
<span data-ttu-id="2e6bd-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e6bd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e6bd-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e6bd-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e6bd-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2e6bd-126">INPUTS</span></span>

### <span data-ttu-id="2e6bd-127">Keine</span><span class="sxs-lookup"><span data-stu-id="2e6bd-127">None</span></span>

## <span data-ttu-id="2e6bd-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2e6bd-128">OUTPUTS</span></span>

### <span data-ttu-id="2e6bd-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2e6bd-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="2e6bd-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2e6bd-130">NOTES</span></span>

## <span data-ttu-id="2e6bd-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2e6bd-131">RELATED LINKS</span></span>

[<span data-ttu-id="2e6bd-132">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2e6bd-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="2e6bd-133">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2e6bd-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="2e6bd-134">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2e6bd-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


