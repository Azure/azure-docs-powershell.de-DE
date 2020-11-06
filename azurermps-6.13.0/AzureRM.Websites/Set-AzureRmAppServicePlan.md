---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 2163c18fecadba069b7c3fba260ab81538ed5583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497142"
---
# <span data-ttu-id="10b15-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="10b15-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="10b15-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="10b15-102">SYNOPSIS</span></span>
<span data-ttu-id="10b15-103">Legt einen Azure-App-Service Plan fest.</span><span class="sxs-lookup"><span data-stu-id="10b15-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10b15-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="10b15-104">SYNTAX</span></span>

### <span data-ttu-id="10b15-105">S1</span><span class="sxs-lookup"><span data-stu-id="10b15-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10b15-106">S2</span><span class="sxs-lookup"><span data-stu-id="10b15-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10b15-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10b15-107">DESCRIPTION</span></span>
<span data-ttu-id="10b15-108">Das Cmdlet " **Set-AzureRmAppServicePlan** " legt einen Azure App-Service Plan fest.</span><span class="sxs-lookup"><span data-stu-id="10b15-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="10b15-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="10b15-109">EXAMPLES</span></span>

### <span data-ttu-id="10b15-110">1: Ändern eines App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="10b15-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="10b15-111">Mit diesem Befehl wird die PerSiteScaling-Option für den App-Dienstplan mit dem Namen ContosoASP, der zur Ressourcengruppe Default-Web-westus gehört, auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="10b15-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="10b15-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="10b15-112">PARAMETERS</span></span>

### <span data-ttu-id="10b15-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="10b15-113">-AdminSiteName</span></span>
<span data-ttu-id="10b15-114">Name der Administratorwebsite</span><span class="sxs-lookup"><span data-stu-id="10b15-114">Admin Site Name</span></span>

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

### <span data-ttu-id="10b15-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="10b15-115">-AppServicePlan</span></span>
<span data-ttu-id="10b15-116">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="10b15-116">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10b15-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10b15-117">-AsJob</span></span>
<span data-ttu-id="10b15-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="10b15-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b15-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10b15-119">-DefaultProfile</span></span>
<span data-ttu-id="10b15-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="10b15-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10b15-121">-Name</span><span class="sxs-lookup"><span data-stu-id="10b15-121">-Name</span></span>
<span data-ttu-id="10b15-122">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="10b15-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="10b15-123">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="10b15-123">-NumberofWorkers</span></span>
<span data-ttu-id="10b15-124">Anzahl der Arbeitskräfte</span><span class="sxs-lookup"><span data-stu-id="10b15-124">Number Of Workers</span></span>

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

### <span data-ttu-id="10b15-125">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="10b15-125">-PerSiteScaling</span></span>
<span data-ttu-id="10b15-126">Pro-Site-Skalierungs boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="10b15-126">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="10b15-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10b15-127">-ResourceGroupName</span></span>
<span data-ttu-id="10b15-128">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="10b15-128">Resource Group Name</span></span>

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

### <span data-ttu-id="10b15-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="10b15-129">-Tier</span></span>
<span data-ttu-id="10b15-130">Ebene</span><span class="sxs-lookup"><span data-stu-id="10b15-130">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b15-131">-Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="10b15-131">-WorkerSize</span></span>
<span data-ttu-id="10b15-132">Workergröße</span><span class="sxs-lookup"><span data-stu-id="10b15-132">Worker Size</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b15-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10b15-133">CommonParameters</span></span>
<span data-ttu-id="10b15-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10b15-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10b15-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10b15-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10b15-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="10b15-136">INPUTS</span></span>

### <span data-ttu-id="10b15-137">Microsoft. Azure. Management. Websites. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="10b15-137">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="10b15-138">Parameter: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="10b15-138">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="10b15-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="10b15-139">OUTPUTS</span></span>

### <span data-ttu-id="10b15-140">Microsoft. Azure. Management. Websites. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="10b15-140">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>

## <span data-ttu-id="10b15-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="10b15-141">NOTES</span></span>

## <span data-ttu-id="10b15-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="10b15-142">RELATED LINKS</span></span>

[<span data-ttu-id="10b15-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="10b15-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="10b15-144">Neu – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="10b15-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="10b15-145">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="10b15-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="10b15-146">Neustart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="10b15-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="10b15-147">Anfang-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="10b15-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="10b15-148">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="10b15-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


