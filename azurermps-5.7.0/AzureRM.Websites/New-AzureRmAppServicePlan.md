---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
ms.openlocfilehash: 09491e82a1eb0ab6b77a382fc727d385bbd6820f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664144"
---
# <span data-ttu-id="2c67a-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2c67a-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="2c67a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c67a-102">SYNOPSIS</span></span>
<span data-ttu-id="2c67a-103">Erstellt einen Azure App-Service Plan an einem bestimmten Geo-Standort.</span><span class="sxs-lookup"><span data-stu-id="2c67a-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c67a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c67a-104">SYNTAX</span></span>

### <span data-ttu-id="2c67a-105">S1</span><span class="sxs-lookup"><span data-stu-id="2c67a-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob][-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c67a-106">S2</span><span class="sxs-lookup"><span data-stu-id="2c67a-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c67a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c67a-107">DESCRIPTION</span></span>
<span data-ttu-id="2c67a-108">Mit dem Cmdlet **New-AzureRmAppServicePlan** wird ein Azure App-Dienstplan an einem bestimmten Geo-Standort mit der angegebenen Ebene, der Arbeitsgröße und der Anzahl der Arbeitskräfte erstellt.</span><span class="sxs-lookup"><span data-stu-id="2c67a-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="2c67a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c67a-109">EXAMPLES</span></span>

### <span data-ttu-id="2c67a-110">Beispiel 1: Erstellen eines App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="2c67a-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="2c67a-111">Dieser Befehl erstellt einen app-Dienstplan mit dem Namen ContosoASP in der Ressourcengruppe Default-Web-westus in Geo-Standort West USA.</span><span class="sxs-lookup"><span data-stu-id="2c67a-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="2c67a-112">Der Befehl gibt eine grundlegende Ebene an und ordnet zwei kleine Arbeitskräfte zu.</span><span class="sxs-lookup"><span data-stu-id="2c67a-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="2c67a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c67a-113">PARAMETERS</span></span>

### <span data-ttu-id="2c67a-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2c67a-114">-AppServicePlan</span></span>
<span data-ttu-id="2c67a-115">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="2c67a-115">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c67a-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="2c67a-116">-AseName</span></span>
<span data-ttu-id="2c67a-117">Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="2c67a-117">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c67a-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c67a-118">-AseResourceGroupName</span></span>
<span data-ttu-id="2c67a-119">Ressourcengruppen Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="2c67a-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c67a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c67a-120">-DefaultProfile</span></span>
<span data-ttu-id="2c67a-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c67a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c67a-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="2c67a-122">-Location</span></span>
<span data-ttu-id="2c67a-123">Lage</span><span class="sxs-lookup"><span data-stu-id="2c67a-123">Location</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c67a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2c67a-124">-Name</span></span>
<span data-ttu-id="2c67a-125">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="2c67a-125">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c67a-126">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="2c67a-126">-NumberofWorkers</span></span>
<span data-ttu-id="2c67a-127">Anzahl der Arbeitskräfte</span><span class="sxs-lookup"><span data-stu-id="2c67a-127">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c67a-128">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="2c67a-128">-PerSiteScaling</span></span>
<span data-ttu-id="2c67a-129">Ob pro Website Skalierung aktiviert werden soll</span><span class="sxs-lookup"><span data-stu-id="2c67a-129">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c67a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c67a-130">-ResourceGroupName</span></span>
<span data-ttu-id="2c67a-131">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="2c67a-131">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c67a-132">-Tier</span><span class="sxs-lookup"><span data-stu-id="2c67a-132">-Tier</span></span>
<span data-ttu-id="2c67a-133">Ebene</span><span class="sxs-lookup"><span data-stu-id="2c67a-133">Tier</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c67a-134">-Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="2c67a-134">-WorkerSize</span></span>
<span data-ttu-id="2c67a-135">Größe des Web Worker</span><span class="sxs-lookup"><span data-stu-id="2c67a-135">Size of web worker</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="2c67a-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c67a-136">-AsJob</span></span>
<span data-ttu-id="2c67a-137">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2c67a-137">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c67a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c67a-138">CommonParameters</span></span>
<span data-ttu-id="2c67a-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c67a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c67a-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c67a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c67a-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c67a-141">INPUTS</span></span>

### <span data-ttu-id="2c67a-142">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="2c67a-142">ServerFarmWithRichSku</span></span>
<span data-ttu-id="2c67a-143">Der Parameter "AppServicePlan" akzeptiert den Wert vom Typ "ServerFarmWithRichSku" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2c67a-143">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="2c67a-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c67a-144">OUTPUTS</span></span>

### <span data-ttu-id="2c67a-145">Microsoft. Azure. Management. Websites. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="2c67a-145">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="2c67a-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c67a-146">NOTES</span></span>

## <span data-ttu-id="2c67a-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c67a-147">RELATED LINKS</span></span>

[<span data-ttu-id="2c67a-148">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2c67a-148">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="2c67a-149">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2c67a-149">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="2c67a-150">Satz-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2c67a-150">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


