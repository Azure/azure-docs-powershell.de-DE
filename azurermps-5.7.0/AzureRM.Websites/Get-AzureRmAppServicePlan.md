---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
ms.openlocfilehash: a46d104a6cd5917d6550d6b78d62a6d50581039e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663736"
---
# <span data-ttu-id="39934-101">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="39934-101">Get-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="39934-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39934-102">SYNOPSIS</span></span>
<span data-ttu-id="39934-103">Ruft einen Azure-App-Dienstplan in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="39934-103">Gets an Azure App Service plan in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39934-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39934-104">SYNTAX</span></span>

### <span data-ttu-id="39934-105">S1</span><span class="sxs-lookup"><span data-stu-id="39934-105">S1</span></span>
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39934-106">S2</span><span class="sxs-lookup"><span data-stu-id="39934-106">S2</span></span>
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39934-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39934-107">DESCRIPTION</span></span>
<span data-ttu-id="39934-108">Das Cmdlet " **Get-AzureRmAppServicePlan** " Ruft einen Azure App-Dienstplan in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="39934-108">The **Get-AzureRmAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="39934-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39934-109">EXAMPLES</span></span>

### <span data-ttu-id="39934-110">Beispiel 1: Abrufen eines App-Service Plans aus einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="39934-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="39934-111">Dieser Befehl ruft den App-Dienstplan mit dem Namen ContosoASP ab, der zur Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="39934-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="39934-112">Beispiel 2: Abrufen aller App-Service Pläne an einem Speicherort</span><span class="sxs-lookup"><span data-stu-id="39934-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

<span data-ttu-id="39934-113">Dieser Befehl ruft alle App-Service Pläne ab, die sich in der Region "West USA" befinden.</span><span class="sxs-lookup"><span data-stu-id="39934-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="39934-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="39934-114">PARAMETERS</span></span>

### <span data-ttu-id="39934-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39934-115">-DefaultProfile</span></span>
<span data-ttu-id="39934-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="39934-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39934-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="39934-117">-Location</span></span>
<span data-ttu-id="39934-118">Lage</span><span class="sxs-lookup"><span data-stu-id="39934-118">Location</span></span> 

```yaml
Type: String
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39934-119">-Name</span><span class="sxs-lookup"><span data-stu-id="39934-119">-Name</span></span>
<span data-ttu-id="39934-120">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="39934-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39934-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39934-121">-ResourceGroupName</span></span>
<span data-ttu-id="39934-122">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="39934-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39934-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39934-123">CommonParameters</span></span>
<span data-ttu-id="39934-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39934-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39934-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39934-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39934-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39934-126">INPUTS</span></span>

### <span data-ttu-id="39934-127">Keine</span><span class="sxs-lookup"><span data-stu-id="39934-127">None</span></span>
<span data-ttu-id="39934-128">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="39934-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="39934-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39934-129">OUTPUTS</span></span>

### <span data-ttu-id="39934-130">Microsoft. Azure. Management. Websites. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="39934-130">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="39934-131">Microsoft. Azure. Management. Websites. Models. ServerFarmCollection</span><span class="sxs-lookup"><span data-stu-id="39934-131">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="39934-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="39934-132">NOTES</span></span>

## <span data-ttu-id="39934-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39934-133">RELATED LINKS</span></span>

[<span data-ttu-id="39934-134">Neu – AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="39934-134">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="39934-135">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="39934-135">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="39934-136">Satz-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="39934-136">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


