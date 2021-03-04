---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/new-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
ms.openlocfilehash: 8382358e6bad15948ed8cdfeb904cf8c431bd131
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938952"
---
# <span data-ttu-id="3b0cf-101">New-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="3b0cf-101">New-AzCommunicationService</span></span>

## <span data-ttu-id="3b0cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b0cf-102">SYNOPSIS</span></span>
<span data-ttu-id="3b0cf-103">Erstellen Sie einen neuen CommunicationService, oder aktualisieren Sie einen vorhandenen CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="3b0cf-103">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="3b0cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b0cf-104">SYNTAX</span></span>

```
New-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DataLocation <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3b0cf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b0cf-105">DESCRIPTION</span></span>
<span data-ttu-id="3b0cf-106">Erstellen Sie einen neuen CommunicationService, oder aktualisieren Sie einen vorhandenen CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="3b0cf-106">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="3b0cf-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3b0cf-107">EXAMPLES</span></span>

### <span data-ttu-id="3b0cf-108">Beispiel 1: Erstellen einer ACS-Ressource</span><span class="sxs-lookup"><span data-stu-id="3b0cf-108">Example 1: Create a ACS resource</span></span>
```powershell
PS C:\> New-AzCommunicationService -ResourceGroupName ContosoResourceProvider1 -Name ContosoAcsResource1 -DataLocation UnitedStates -Location Global

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="3b0cf-109">Erstellt eine ACS-Ressource mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="3b0cf-109">Creates a ACS resource using the specified parameters.</span></span>

## <span data-ttu-id="3b0cf-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3b0cf-110">PARAMETERS</span></span>

### <span data-ttu-id="3b0cf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b0cf-111">-AsJob</span></span>
<span data-ttu-id="3b0cf-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="3b0cf-112">Run the command as a job</span></span>

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

### <span data-ttu-id="3b0cf-113">-DataLocation</span><span class="sxs-lookup"><span data-stu-id="3b0cf-113">-DataLocation</span></span>
<span data-ttu-id="3b0cf-114">Der Speicherort, an dem der Kommunikationsdienst seine Ruhedaten speichert.</span><span class="sxs-lookup"><span data-stu-id="3b0cf-114">The location where the communication service stores its data at rest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b0cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b0cf-115">-DefaultProfile</span></span>
<span data-ttu-id="3b0cf-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b0cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b0cf-117">-Location</span><span class="sxs-lookup"><span data-stu-id="3b0cf-117">-Location</span></span>
<span data-ttu-id="3b0cf-118">Der Azure-Speicherort, an dem der CommunicationService ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b0cf-118">The Azure location where the CommunicationService is running.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b0cf-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3b0cf-119">-Name</span></span>
<span data-ttu-id="3b0cf-120">Der Name der CommunicationService-Ressource.</span><span class="sxs-lookup"><span data-stu-id="3b0cf-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b0cf-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3b0cf-121">-NoWait</span></span>
<span data-ttu-id="3b0cf-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="3b0cf-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3b0cf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b0cf-123">-ResourceGroupName</span></span>
<span data-ttu-id="3b0cf-124">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="3b0cf-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3b0cf-125">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="3b0cf-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3b0cf-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3b0cf-126">-SubscriptionId</span></span>
<span data-ttu-id="3b0cf-127">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3b0cf-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3b0cf-128">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="3b0cf-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3b0cf-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b0cf-129">-Tag</span></span>
<span data-ttu-id="3b0cf-130">Tags des Diensts, bei dem es sich um eine Liste von Schlüsselwertpaaren handelt, die die Ressource beschreiben.</span><span class="sxs-lookup"><span data-stu-id="3b0cf-130">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b0cf-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3b0cf-131">-Confirm</span></span>
<span data-ttu-id="3b0cf-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b0cf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b0cf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b0cf-133">-WhatIf</span></span>
<span data-ttu-id="3b0cf-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b0cf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b0cf-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b0cf-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b0cf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b0cf-136">CommonParameters</span></span>
<span data-ttu-id="3b0cf-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b0cf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b0cf-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b0cf-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b0cf-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3b0cf-139">INPUTS</span></span>

## <span data-ttu-id="3b0cf-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3b0cf-140">OUTPUTS</span></span>

### <span data-ttu-id="3b0cf-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="3b0cf-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="3b0cf-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3b0cf-142">NOTES</span></span>

<span data-ttu-id="3b0cf-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="3b0cf-143">ALIASES</span></span>

## <span data-ttu-id="3b0cf-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3b0cf-144">RELATED LINKS</span></span>

