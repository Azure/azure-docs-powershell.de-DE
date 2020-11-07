---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: 064ccbcfa94137f5221a5d08e0a06e09328e0b1f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658579"
---
# <span data-ttu-id="0e6d3-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0e6d3-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="0e6d3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e6d3-102">SYNOPSIS</span></span>
<span data-ttu-id="0e6d3-103">Ruft einen Azure-App-Dienstplan in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="0e6d3-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="0e6d3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e6d3-104">SYNTAX</span></span>

### <span data-ttu-id="0e6d3-105">S1</span><span class="sxs-lookup"><span data-stu-id="0e6d3-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e6d3-106">S2</span><span class="sxs-lookup"><span data-stu-id="0e6d3-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e6d3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e6d3-107">DESCRIPTION</span></span>
<span data-ttu-id="0e6d3-108">Das Cmdlet " **Get-AzAppServicePlan** " Ruft einen Azure App-Dienstplan in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="0e6d3-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="0e6d3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e6d3-109">EXAMPLES</span></span>

### <span data-ttu-id="0e6d3-110">Beispiel 1: Abrufen eines App-Service Plans aus einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0e6d3-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="0e6d3-111">Dieser Befehl ruft den App-Dienstplan mit dem Namen ContosoASP ab, der zur Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="0e6d3-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="0e6d3-112">Beispiel 2: Abrufen aller App-Service Pläne an einem Speicherort</span><span class="sxs-lookup"><span data-stu-id="0e6d3-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="0e6d3-113">Dieser Befehl ruft alle App-Service Pläne ab, die sich in der Region "West USA" befinden.</span><span class="sxs-lookup"><span data-stu-id="0e6d3-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="0e6d3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e6d3-114">PARAMETERS</span></span>

### <span data-ttu-id="0e6d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e6d3-115">-DefaultProfile</span></span>
<span data-ttu-id="0e6d3-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0e6d3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e6d3-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="0e6d3-117">-Location</span></span>
<span data-ttu-id="0e6d3-118">Lage</span><span class="sxs-lookup"><span data-stu-id="0e6d3-118">Location</span></span> 

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

### <span data-ttu-id="0e6d3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0e6d3-119">-Name</span></span>
<span data-ttu-id="0e6d3-120">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="0e6d3-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="0e6d3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e6d3-121">-ResourceGroupName</span></span>
<span data-ttu-id="0e6d3-122">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="0e6d3-122">Resource Group Name</span></span>

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

### <span data-ttu-id="0e6d3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e6d3-123">CommonParameters</span></span>
<span data-ttu-id="0e6d3-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e6d3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e6d3-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e6d3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e6d3-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e6d3-126">INPUTS</span></span>

### <span data-ttu-id="0e6d3-127">Keine</span><span class="sxs-lookup"><span data-stu-id="0e6d3-127">None</span></span>

## <span data-ttu-id="0e6d3-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e6d3-128">OUTPUTS</span></span>

### <span data-ttu-id="0e6d3-129">Microsoft. Azure. Commands. webapps. Models. PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="0e6d3-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="0e6d3-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e6d3-130">NOTES</span></span>

## <span data-ttu-id="0e6d3-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e6d3-131">RELATED LINKS</span></span>

[<span data-ttu-id="0e6d3-132">Neu – AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0e6d3-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="0e6d3-133">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0e6d3-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="0e6d3-134">Satz-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0e6d3-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


