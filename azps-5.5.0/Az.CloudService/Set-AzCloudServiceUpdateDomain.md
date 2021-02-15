---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/set-azcloudserviceupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Set-AzCloudServiceUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Set-AzCloudServiceUpdateDomain.md
ms.openlocfilehash: 4ffb65d4eca9511e179d33c53cb8f515c28aab58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171372"
---
# <span data-ttu-id="ba91e-101">Set-AzCloudServiceUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="ba91e-101">Set-AzCloudServiceUpdateDomain</span></span>

## <span data-ttu-id="ba91e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba91e-102">SYNOPSIS</span></span>
<span data-ttu-id="ba91e-103">Aktualisiert die Rolleninstanzen in der angegebenen Updatedomäne.</span><span class="sxs-lookup"><span data-stu-id="ba91e-103">Updates the role instances in the specified update domain.</span></span>

## <span data-ttu-id="ba91e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba91e-104">SYNTAX</span></span>

```
Set-AzCloudServiceUpdateDomain -CloudServiceName <String> -ResourceGroupName <String> -UpdateDomain <Int32>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ba91e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba91e-105">DESCRIPTION</span></span>
<span data-ttu-id="ba91e-106">Aktualisiert die Rolleninstanzen in der angegebenen Updatedomäne.</span><span class="sxs-lookup"><span data-stu-id="ba91e-106">Updates the role instances in the specified update domain.</span></span>

## <span data-ttu-id="ba91e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ba91e-107">EXAMPLES</span></span>

### <span data-ttu-id="ba91e-108">Beispiel 1: Aktualisieren der Rolleninstanz in der Updatedomäne</span><span class="sxs-lookup"><span data-stu-id="ba91e-108">Example 1: Update role instance in update domain</span></span>
```powershell
PS C:\> Set-AzCloudServiceUpdateDomain -CloudServiceName "ContosoCS" -ResourceGroupName "ContosOrg" -UpdateDomain 0
```

<span data-ttu-id="ba91e-109">Mit diesem Befehl werden Rolleninstanzen in der Updatedomäne 0 des Clouddiensts "ContosoCS" aktualisiert, der zur Ressourcengruppe "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="ba91e-109">This command updates role instances in update domain 0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="ba91e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba91e-110">PARAMETERS</span></span>

### <span data-ttu-id="ba91e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba91e-111">-AsJob</span></span>
<span data-ttu-id="ba91e-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="ba91e-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ba91e-113">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="ba91e-113">-CloudServiceName</span></span>
<span data-ttu-id="ba91e-114">Der Name des Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="ba91e-114">Name of the cloud service.</span></span>

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

### <span data-ttu-id="ba91e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba91e-115">-DefaultProfile</span></span>
<span data-ttu-id="ba91e-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba91e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba91e-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ba91e-117">-NoWait</span></span>
<span data-ttu-id="ba91e-118">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="ba91e-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ba91e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba91e-119">-PassThru</span></span>
<span data-ttu-id="ba91e-120">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ba91e-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ba91e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba91e-121">-ResourceGroupName</span></span>
<span data-ttu-id="ba91e-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ba91e-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="ba91e-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba91e-123">-SubscriptionId</span></span>
<span data-ttu-id="ba91e-124">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ba91e-124">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ba91e-125">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="ba91e-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ba91e-126">-UpdateDomain</span><span class="sxs-lookup"><span data-stu-id="ba91e-126">-UpdateDomain</span></span>
<span data-ttu-id="ba91e-127">Gibt einen ganzzahligen Wert an, der die Updatedomäne identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ba91e-127">Specifies an integer value that identifies the update domain.</span></span>
<span data-ttu-id="ba91e-128">Updatedomänen werden mit einem nullbasierten Index identifiziert: Die erste Updatedomäne hat die ID 0, die zweite die ID 1 und so weiter.</span><span class="sxs-lookup"><span data-stu-id="ba91e-128">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba91e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba91e-129">-Confirm</span></span>
<span data-ttu-id="ba91e-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba91e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba91e-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ba91e-131">-WhatIf</span></span>
<span data-ttu-id="ba91e-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba91e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba91e-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba91e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba91e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba91e-134">CommonParameters</span></span>
<span data-ttu-id="ba91e-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba91e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba91e-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba91e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba91e-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ba91e-137">INPUTS</span></span>

## <span data-ttu-id="ba91e-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ba91e-138">OUTPUTS</span></span>

### <span data-ttu-id="ba91e-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ba91e-139">System.Boolean</span></span>

## <span data-ttu-id="ba91e-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ba91e-140">NOTES</span></span>

<span data-ttu-id="ba91e-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ba91e-141">ALIASES</span></span>

## <span data-ttu-id="ba91e-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ba91e-142">RELATED LINKS</span></span>

