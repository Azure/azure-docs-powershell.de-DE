---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 4b6270a6d56b8f210b2f03311bf19bb09950f361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479822"
---
# <span data-ttu-id="ac794-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ac794-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="ac794-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac794-102">SYNOPSIS</span></span>
<span data-ttu-id="ac794-103">Legt einen Azure-App-Service Plan fest.</span><span class="sxs-lookup"><span data-stu-id="ac794-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac794-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac794-104">SYNTAX</span></span>

### <span data-ttu-id="ac794-105">S1</span><span class="sxs-lookup"><span data-stu-id="ac794-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac794-106">S2</span><span class="sxs-lookup"><span data-stu-id="ac794-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac794-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac794-107">DESCRIPTION</span></span>
<span data-ttu-id="ac794-108">Das Cmdlet " **Set-AzureRmAppServicePlan** " legt einen Azure App-Service Plan fest.</span><span class="sxs-lookup"><span data-stu-id="ac794-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="ac794-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac794-109">EXAMPLES</span></span>

### <span data-ttu-id="ac794-110">1: Ändern eines App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="ac794-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="ac794-111">Mit diesem Befehl wird die PerSiteScaling-Option für den App-Dienstplan mit dem Namen ContosoASP, der zur Ressourcengruppe Default-Web-westus gehört, auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ac794-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ac794-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac794-112">PARAMETERS</span></span>

### <span data-ttu-id="ac794-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="ac794-113">-AdminSiteName</span></span>
<span data-ttu-id="ac794-114">Name der Administratorwebsite</span><span class="sxs-lookup"><span data-stu-id="ac794-114">Admin Site Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac794-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ac794-115">-AppServicePlan</span></span>
<span data-ttu-id="ac794-116">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="ac794-116">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac794-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ac794-117">-Name</span></span>
<span data-ttu-id="ac794-118">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="ac794-118">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac794-119">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="ac794-119">-NumberofWorkers</span></span>
<span data-ttu-id="ac794-120">Anzahl der Arbeitskräfte</span><span class="sxs-lookup"><span data-stu-id="ac794-120">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac794-121">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="ac794-121">-PerSiteScaling</span></span>
<span data-ttu-id="ac794-122">Pro-Site-Skalierungs boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="ac794-122">Per Site Scaling Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac794-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac794-123">-ResourceGroupName</span></span>
<span data-ttu-id="ac794-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="ac794-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac794-125">-Tier</span><span class="sxs-lookup"><span data-stu-id="ac794-125">-Tier</span></span>
<span data-ttu-id="ac794-126">Ebene</span><span class="sxs-lookup"><span data-stu-id="ac794-126">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac794-127">-Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="ac794-127">-WorkerSize</span></span>
<span data-ttu-id="ac794-128">Workergröße</span><span class="sxs-lookup"><span data-stu-id="ac794-128">Worker Size</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac794-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac794-129">-DefaultProfile</span></span>
<span data-ttu-id="ac794-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ac794-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac794-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac794-131">CommonParameters</span></span>
<span data-ttu-id="ac794-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac794-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac794-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac794-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac794-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac794-134">INPUTS</span></span>

### <span data-ttu-id="ac794-135">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="ac794-135">ServerFarmWithRichSku</span></span>
<span data-ttu-id="ac794-136">Der Parameter "AppServicePlan" akzeptiert den Wert vom Typ "ServerFarmWithRichSku" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ac794-136">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="ac794-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac794-137">OUTPUTS</span></span>

### <span data-ttu-id="ac794-138">Microsoft. Azure. Management. Websites. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="ac794-138">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="ac794-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac794-139">NOTES</span></span>

## <span data-ttu-id="ac794-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac794-140">RELATED LINKS</span></span>

[<span data-ttu-id="ac794-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ac794-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="ac794-142">Neu – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ac794-142">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="ac794-143">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ac794-143">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="ac794-144">Neustart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ac794-144">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="ac794-145">Anfang-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ac794-145">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="ac794-146">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ac794-146">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


