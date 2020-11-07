---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: d27dc8ae315eb587ccb129125500a86e22429773
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658505"
---
# <span data-ttu-id="b2684-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b2684-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="b2684-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2684-102">SYNOPSIS</span></span>
<span data-ttu-id="b2684-103">Legt einen Azure-App-Service Plan fest.</span><span class="sxs-lookup"><span data-stu-id="b2684-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="b2684-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2684-104">SYNTAX</span></span>

### <span data-ttu-id="b2684-105">S1</span><span class="sxs-lookup"><span data-stu-id="b2684-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2684-106">S2</span><span class="sxs-lookup"><span data-stu-id="b2684-106">S2</span></span>
```
Set-AzAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2684-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2684-107">DESCRIPTION</span></span>
<span data-ttu-id="b2684-108">Das Cmdlet " **Set-AzAppServicePlan** " legt einen Azure App-Service Plan fest.</span><span class="sxs-lookup"><span data-stu-id="b2684-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="b2684-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2684-109">EXAMPLES</span></span>

### <span data-ttu-id="b2684-110">1: Ändern eines App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="b2684-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="b2684-111">Mit diesem Befehl wird die PerSiteScaling-Option für den App-Dienstplan mit dem Namen ContosoASP, der zur Ressourcengruppe Default-Web-westus gehört, auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b2684-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="b2684-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2684-112">PARAMETERS</span></span>

### <span data-ttu-id="b2684-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="b2684-113">-AdminSiteName</span></span>
<span data-ttu-id="b2684-114">Name der Administratorwebsite</span><span class="sxs-lookup"><span data-stu-id="b2684-114">Admin Site Name</span></span>

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

### <span data-ttu-id="b2684-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b2684-115">-AppServicePlan</span></span>
<span data-ttu-id="b2684-116">App-Service Plan Objekt</span><span class="sxs-lookup"><span data-stu-id="b2684-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="b2684-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2684-117">-AsJob</span></span>
<span data-ttu-id="b2684-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b2684-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2684-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2684-119">-DefaultProfile</span></span>
<span data-ttu-id="b2684-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b2684-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2684-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b2684-121">-Name</span></span>
<span data-ttu-id="b2684-122">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="b2684-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="b2684-123">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="b2684-123">-NumberofWorkers</span></span>
<span data-ttu-id="b2684-124">Anzahl der Arbeitskräfte</span><span class="sxs-lookup"><span data-stu-id="b2684-124">Number Of Workers</span></span>

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

### <span data-ttu-id="b2684-125">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="b2684-125">-PerSiteScaling</span></span>
<span data-ttu-id="b2684-126">Pro-Site-Skalierungs boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="b2684-126">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="b2684-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2684-127">-ResourceGroupName</span></span>
<span data-ttu-id="b2684-128">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="b2684-128">Resource Group Name</span></span>

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

### <span data-ttu-id="b2684-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="b2684-129">-Tier</span></span>
<span data-ttu-id="b2684-130">Ebene</span><span class="sxs-lookup"><span data-stu-id="b2684-130">Tier</span></span>

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

### <span data-ttu-id="b2684-131">-Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="b2684-131">-WorkerSize</span></span>
<span data-ttu-id="b2684-132">Workergröße</span><span class="sxs-lookup"><span data-stu-id="b2684-132">Worker Size</span></span>

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

### <span data-ttu-id="b2684-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2684-133">CommonParameters</span></span>
<span data-ttu-id="b2684-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2684-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2684-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2684-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2684-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2684-136">INPUTS</span></span>

### <span data-ttu-id="b2684-137">Microsoft. Azure. Commands. webapps. Models. PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="b2684-137">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="b2684-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2684-138">OUTPUTS</span></span>

### <span data-ttu-id="b2684-139">Microsoft. Azure. Commands. webapps. Models. PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="b2684-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="b2684-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2684-140">NOTES</span></span>

## <span data-ttu-id="b2684-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2684-141">RELATED LINKS</span></span>

[<span data-ttu-id="b2684-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b2684-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="b2684-143">Neu – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b2684-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="b2684-144">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b2684-144">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="b2684-145">Neustart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b2684-145">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="b2684-146">Anfang-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b2684-146">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="b2684-147">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b2684-147">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


