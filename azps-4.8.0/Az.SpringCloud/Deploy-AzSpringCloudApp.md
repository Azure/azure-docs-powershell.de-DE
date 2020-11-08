---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: 8a80c323f1cf1d8d015faeda6541b77667a6ca19
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166076"
---
# <span data-ttu-id="7551d-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="7551d-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="7551d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7551d-102">SYNOPSIS</span></span>
<span data-ttu-id="7551d-103">Stellen Sie das integrierte jar für den Service bereit.</span><span class="sxs-lookup"><span data-stu-id="7551d-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="7551d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7551d-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7551d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7551d-105">DESCRIPTION</span></span>
<span data-ttu-id="7551d-106">Stellen Sie das integrierte jar für den Service bereit.</span><span class="sxs-lookup"><span data-stu-id="7551d-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="7551d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7551d-107">EXAMPLES</span></span>

### <span data-ttu-id="7551d-108">Beispiel 1: Bereitstellen des lokalen kompilierten jar-Diensts nach Namen.</span><span class="sxs-lookup"><span data-stu-id="7551d-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="7551d-109">Bereitstellen des lokalen kompilierten jar-Diensts nach Name</span><span class="sxs-lookup"><span data-stu-id="7551d-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="7551d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7551d-110">PARAMETERS</span></span>

### <span data-ttu-id="7551d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7551d-111">-AsJob</span></span>
<span data-ttu-id="7551d-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="7551d-112">Run the command as a job</span></span>

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

### <span data-ttu-id="7551d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7551d-113">-DefaultProfile</span></span>
<span data-ttu-id="7551d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7551d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7551d-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="7551d-115">-JarPath</span></span>
<span data-ttu-id="7551d-116">Der Pfad des jar muss deploied sein.</span><span class="sxs-lookup"><span data-stu-id="7551d-116">The path of the jar need to be deploied.</span></span>

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

### <span data-ttu-id="7551d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7551d-117">-Name</span></span>
<span data-ttu-id="7551d-118">Der Name der APP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="7551d-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="7551d-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="7551d-119">-NoWait</span></span>
<span data-ttu-id="7551d-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="7551d-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7551d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7551d-121">-ResourceGroupName</span></span>
<span data-ttu-id="7551d-122">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="7551d-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7551d-123">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="7551d-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7551d-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7551d-124">-ServiceName</span></span>
<span data-ttu-id="7551d-125">Der Name der Dienstressource.</span><span class="sxs-lookup"><span data-stu-id="7551d-125">The name of the Service resource.</span></span>

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

### <span data-ttu-id="7551d-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="7551d-126">-SubscriptionId</span></span>
<span data-ttu-id="7551d-127">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7551d-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7551d-128">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="7551d-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7551d-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7551d-129">-Confirm</span></span>
<span data-ttu-id="7551d-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7551d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7551d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7551d-131">-WhatIf</span></span>
<span data-ttu-id="7551d-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7551d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7551d-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7551d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7551d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7551d-134">CommonParameters</span></span>
<span data-ttu-id="7551d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7551d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7551d-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7551d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7551d-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7551d-137">INPUTS</span></span>

## <span data-ttu-id="7551d-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7551d-138">OUTPUTS</span></span>

### <span data-ttu-id="7551d-139">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20190501Preview. IAppResource</span><span class="sxs-lookup"><span data-stu-id="7551d-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IAppResource</span></span>

## <span data-ttu-id="7551d-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="7551d-140">NOTES</span></span>

<span data-ttu-id="7551d-141">Aliase</span><span class="sxs-lookup"><span data-stu-id="7551d-141">ALIASES</span></span>

## <span data-ttu-id="7551d-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7551d-142">RELATED LINKS</span></span>

