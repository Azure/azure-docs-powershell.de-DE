---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
ms.openlocfilehash: ae630f053f6267a49477118786cf70b65782d68e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298935"
---
# <span data-ttu-id="8451f-101">New-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="8451f-101">New-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="8451f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8451f-102">SYNOPSIS</span></span>
<span data-ttu-id="8451f-103">Erstellen oder Aktualisieren einer Zuordnung</span><span class="sxs-lookup"><span data-stu-id="8451f-103">Create or update an association.</span></span>

## <span data-ttu-id="8451f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8451f-104">SYNTAX</span></span>

```
New-AzCustomProviderAssociation -Name <String> -Scope <String> [-TargetResourceId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8451f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8451f-105">DESCRIPTION</span></span>
<span data-ttu-id="8451f-106">Erstellen oder Aktualisieren einer Zuordnung</span><span class="sxs-lookup"><span data-stu-id="8451f-106">Create or update an association.</span></span>

## <span data-ttu-id="8451f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8451f-107">EXAMPLES</span></span>

### <span data-ttu-id="8451f-108">Beispiel 1: Erstellen einer benutzerdefinierten Anbieter Zuordnung</span><span class="sxs-lookup"><span data-stu-id="8451f-108">Example 1: Create a custom provider association</span></span>
```powershell
PS C:\> $provider = Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
PS C:\> New-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc -TargetResourceId $provider.Id

Location  Name     Type
--------  ----     ----
East US 2 MyAssoc  Microsoft.CustomProviders/associations
```

<span data-ttu-id="8451f-109">Erstellen einer benutzerdefinierten Anbieter Zuordnung muss das zugeordnete Ziel provioder ordnungsgemäß mit einer Route für "Assoziationen" konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="8451f-109">Create a custom provider association, the associated target provioder must be properly configured with a route for "associations"</span></span>

## <span data-ttu-id="8451f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8451f-110">PARAMETERS</span></span>

### <span data-ttu-id="8451f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8451f-111">-AsJob</span></span>
<span data-ttu-id="8451f-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="8451f-112">Run the command as a job</span></span>

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

### <span data-ttu-id="8451f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8451f-113">-DefaultProfile</span></span>
<span data-ttu-id="8451f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8451f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8451f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8451f-115">-Name</span></span>
<span data-ttu-id="8451f-116">Der Name der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="8451f-116">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8451f-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8451f-117">-NoWait</span></span>
<span data-ttu-id="8451f-118">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="8451f-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8451f-119">-Scope</span><span class="sxs-lookup"><span data-stu-id="8451f-119">-Scope</span></span>
<span data-ttu-id="8451f-120">Der Bereich der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="8451f-120">The scope of the association.</span></span>
<span data-ttu-id="8451f-121">Der Bereich kann eine beliebige gültige Ruhezeit-Ressourceninstanz sein.</span><span class="sxs-lookup"><span data-stu-id="8451f-121">The scope can be any valid REST resource instance.</span></span>
<span data-ttu-id="8451f-122">Verwenden Sie beispielsweise "/Subscriptions/{Subscription-ID}/resourceGroups/{Resource-Group-Name}/Providers/Microsoft.Compute/virtualMachines/{VM-Name}" für eine Ressource einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="8451f-122">For example, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' for a virtual machine resource.</span></span>

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

### <span data-ttu-id="8451f-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="8451f-123">-TargetResourceId</span></span>
<span data-ttu-id="8451f-124">Die restliche Ressourceninstanz der Zielressource für diese Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="8451f-124">The REST resource instance of the target resource for this association.</span></span>

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

### <span data-ttu-id="8451f-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8451f-125">-Confirm</span></span>
<span data-ttu-id="8451f-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8451f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8451f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8451f-127">-WhatIf</span></span>
<span data-ttu-id="8451f-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8451f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8451f-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8451f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8451f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8451f-130">CommonParameters</span></span>
<span data-ttu-id="8451f-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8451f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8451f-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8451f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8451f-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8451f-133">INPUTS</span></span>

## <span data-ttu-id="8451f-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8451f-134">OUTPUTS</span></span>

### <span data-ttu-id="8451f-135">Microsoft. Azure. PowerShell. Cmdlets. CustomProviders. Models. Api20180901Preview. IAssociation</span><span class="sxs-lookup"><span data-stu-id="8451f-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="8451f-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="8451f-136">NOTES</span></span>

<span data-ttu-id="8451f-137">Aliase</span><span class="sxs-lookup"><span data-stu-id="8451f-137">ALIASES</span></span>

## <span data-ttu-id="8451f-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8451f-138">RELATED LINKS</span></span>

