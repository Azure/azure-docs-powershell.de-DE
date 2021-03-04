---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: 96b3b3fcb2fcea50e1607c67d98079e5d1600f4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920280"
---
# <span data-ttu-id="d6885-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="d6885-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="d6885-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6885-102">SYNOPSIS</span></span>
<span data-ttu-id="d6885-103">Stellen Sie das integrierte Jar für den Dienst zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d6885-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="d6885-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6885-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d6885-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d6885-105">DESCRIPTION</span></span>
<span data-ttu-id="d6885-106">Stellen Sie das integrierte Jar für den Dienst zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d6885-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="d6885-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d6885-107">EXAMPLES</span></span>

### <span data-ttu-id="d6885-108">Beispiel 1: Bereitstellen des lokalen kompilierten Jars für den Dienst nach Name.</span><span class="sxs-lookup"><span data-stu-id="d6885-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="d6885-109">Stellen Sie den lokalen kompilierten Jar für den Dienst nach Name zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d6885-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="d6885-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d6885-110">PARAMETERS</span></span>

### <span data-ttu-id="d6885-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6885-111">-AsJob</span></span>
<span data-ttu-id="d6885-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="d6885-112">Run the command as a job</span></span>

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

### <span data-ttu-id="d6885-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6885-113">-DefaultProfile</span></span>
<span data-ttu-id="d6885-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6885-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6885-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="d6885-115">-JarPath</span></span>
<span data-ttu-id="d6885-116">Der Pfad des Jars muss beklagen.</span><span class="sxs-lookup"><span data-stu-id="d6885-116">The path of the jar need to be deploied.</span></span>

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

### <span data-ttu-id="d6885-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d6885-117">-Name</span></span>
<span data-ttu-id="d6885-118">Der Name der App-Ressource.</span><span class="sxs-lookup"><span data-stu-id="d6885-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="d6885-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d6885-119">-NoWait</span></span>
<span data-ttu-id="d6885-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="d6885-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d6885-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6885-121">-ResourceGroupName</span></span>
<span data-ttu-id="d6885-122">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="d6885-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d6885-123">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="d6885-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d6885-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d6885-124">-ServiceName</span></span>
<span data-ttu-id="d6885-125">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="d6885-125">The name of the Service resource.</span></span>

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

### <span data-ttu-id="d6885-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6885-126">-SubscriptionId</span></span>
<span data-ttu-id="d6885-127">Ruft die Abonnement-ID ab, mit der das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="d6885-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d6885-128">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="d6885-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d6885-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d6885-129">-Confirm</span></span>
<span data-ttu-id="d6885-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d6885-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6885-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6885-131">-WhatIf</span></span>
<span data-ttu-id="d6885-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d6885-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6885-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6885-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6885-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6885-134">CommonParameters</span></span>
<span data-ttu-id="d6885-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6885-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6885-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6885-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6885-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d6885-137">INPUTS</span></span>

## <span data-ttu-id="d6885-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d6885-138">OUTPUTS</span></span>

### <span data-ttu-id="d6885-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="d6885-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="d6885-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d6885-140">NOTES</span></span>

<span data-ttu-id="d6885-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d6885-141">ALIASES</span></span>

## <span data-ttu-id="d6885-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d6885-142">RELATED LINKS</span></span>

