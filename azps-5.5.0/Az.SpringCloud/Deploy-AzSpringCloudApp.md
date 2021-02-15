---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: c6a7381c993b52995ab39a60fde54900092a5915
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173916"
---
# <span data-ttu-id="75444-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="75444-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="75444-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75444-102">SYNOPSIS</span></span>
<span data-ttu-id="75444-103">Stellen Sie die integrierte Jar-To-Service-Lösung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="75444-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="75444-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75444-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="75444-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75444-105">DESCRIPTION</span></span>
<span data-ttu-id="75444-106">Stellen Sie die integrierte Jar-To-Service-Lösung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="75444-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="75444-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="75444-107">EXAMPLES</span></span>

### <span data-ttu-id="75444-108">Beispiel 1: Bereitstellen von lokal kompilierten Jars nach Name.</span><span class="sxs-lookup"><span data-stu-id="75444-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="75444-109">Stellen Sie lokal kompilierte Jar zum Service nach Name zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="75444-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="75444-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75444-110">PARAMETERS</span></span>

### <span data-ttu-id="75444-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75444-111">-AsJob</span></span>
<span data-ttu-id="75444-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="75444-112">Run the command as a job</span></span>

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

### <span data-ttu-id="75444-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75444-113">-DefaultProfile</span></span>
<span data-ttu-id="75444-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="75444-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75444-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="75444-115">-JarPath</span></span>
<span data-ttu-id="75444-116">Der Pfad des Glases muss verdingt werden.</span><span class="sxs-lookup"><span data-stu-id="75444-116">The path of the jar need to be deploied.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75444-117">-Name</span><span class="sxs-lookup"><span data-stu-id="75444-117">-Name</span></span>
<span data-ttu-id="75444-118">Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="75444-118">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75444-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="75444-119">-NoWait</span></span>
<span data-ttu-id="75444-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="75444-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="75444-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75444-121">-ResourceGroupName</span></span>
<span data-ttu-id="75444-122">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="75444-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="75444-123">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="75444-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75444-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="75444-124">-ServiceName</span></span>
<span data-ttu-id="75444-125">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="75444-125">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75444-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75444-126">-SubscriptionId</span></span>
<span data-ttu-id="75444-127">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="75444-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="75444-128">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="75444-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75444-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75444-129">-Confirm</span></span>
<span data-ttu-id="75444-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75444-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75444-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="75444-131">-WhatIf</span></span>
<span data-ttu-id="75444-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75444-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75444-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75444-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75444-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75444-134">CommonParameters</span></span>
<span data-ttu-id="75444-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75444-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75444-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75444-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75444-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="75444-137">INPUTS</span></span>

## <span data-ttu-id="75444-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="75444-138">OUTPUTS</span></span>

### <span data-ttu-id="75444-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="75444-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="75444-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="75444-140">NOTES</span></span>

<span data-ttu-id="75444-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="75444-141">ALIASES</span></span>

## <span data-ttu-id="75444-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="75444-142">RELATED LINKS</span></span>

