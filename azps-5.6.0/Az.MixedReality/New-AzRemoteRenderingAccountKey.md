---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/new-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: 8bfc07b5502c2dd648beea827af9587c9e6d9447
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927880"
---
# <span data-ttu-id="e4ca1-101">New-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="e4ca1-101">New-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="e4ca1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4ca1-102">SYNOPSIS</span></span>
<span data-ttu-id="e4ca1-103">Schlüssel zum Erneuten Erstellen des Remoterenderingkontos</span><span class="sxs-lookup"><span data-stu-id="e4ca1-103">Regenerate key of Remote Rendering Account</span></span>

## <span data-ttu-id="e4ca1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4ca1-104">SYNTAX</span></span>

### <span data-ttu-id="e4ca1-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4ca1-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4ca1-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4ca1-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4ca1-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4ca1-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4ca1-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4ca1-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4ca1-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4ca1-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4ca1-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4ca1-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4ca1-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4ca1-111">DESCRIPTION</span></span>
<span data-ttu-id="e4ca1-112">Regenerieren Sie den Primärschlüssel oder sekundären Schlüssel des Remoterenderingkontos.</span><span class="sxs-lookup"><span data-stu-id="e4ca1-112">Regenerate primary key or secondary key of Remote Rendering Account.</span></span>

## <span data-ttu-id="e4ca1-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e4ca1-113">EXAMPLES</span></span>

### <span data-ttu-id="e4ca1-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e4ca1-114">Example 1</span></span>
```powershell
PS C:\> New-AzRemoteRenderingAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="e4ca1-115">Regenerieren Sie den sekundären Schlüssel des Remoterenderungskontos "Example" in der Ressourcengruppe "rg1".</span><span class="sxs-lookup"><span data-stu-id="e4ca1-115">Regenerate secondary key of Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="e4ca1-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e4ca1-116">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | New-AzRemoteRenderingAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="e4ca1-117">Regenerieren Sie den sekundären Schlüssel des Remoterenderingkontos "Example" aus dem aktuellen Abonnement und der Ressourcengruppe "rg1" mit Piping.</span><span class="sxs-lookup"><span data-stu-id="e4ca1-117">Regenerate secondary key of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="e4ca1-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e4ca1-118">PARAMETERS</span></span>

### <span data-ttu-id="e4ca1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4ca1-119">-DefaultProfile</span></span>
<span data-ttu-id="e4ca1-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4ca1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4ca1-121">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="e4ca1-121">-Force</span></span>
<span data-ttu-id="e4ca1-122">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="e4ca1-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e4ca1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4ca1-123">-InputObject</span></span>
<span data-ttu-id="e4ca1-124">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="e4ca1-124">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4ca1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e4ca1-125">-Name</span></span>
<span data-ttu-id="e4ca1-126">Name des Remoterenderingkontos.</span><span class="sxs-lookup"><span data-stu-id="e4ca1-126">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4ca1-127">-Primär</span><span class="sxs-lookup"><span data-stu-id="e4ca1-127">-Primary</span></span>
<span data-ttu-id="e4ca1-128">Regenerieren Sie den Primärschlüssel des Remoterenderingkontos.</span><span class="sxs-lookup"><span data-stu-id="e4ca1-128">Regenerate primary key of Remote Rendering Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4ca1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4ca1-129">-ResourceGroupName</span></span>
<span data-ttu-id="e4ca1-130">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="e4ca1-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4ca1-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4ca1-131">-ResourceId</span></span>
<span data-ttu-id="e4ca1-132">Ressourcen-ID des Remoterenderingkontos.</span><span class="sxs-lookup"><span data-stu-id="e4ca1-132">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4ca1-133">-Sekundär</span><span class="sxs-lookup"><span data-stu-id="e4ca1-133">-Secondary</span></span>
<span data-ttu-id="e4ca1-134">Regenerieren Sie den Primärschlüssel des Remoterenderingkontos.</span><span class="sxs-lookup"><span data-stu-id="e4ca1-134">Regenerate primary key of Remote Rendering Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4ca1-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e4ca1-135">-Confirm</span></span>
<span data-ttu-id="e4ca1-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e4ca1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4ca1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4ca1-137">-WhatIf</span></span>
<span data-ttu-id="e4ca1-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e4ca1-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4ca1-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e4ca1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4ca1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4ca1-140">CommonParameters</span></span>
<span data-ttu-id="e4ca1-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4ca1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e4ca1-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4ca1-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4ca1-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e4ca1-143">INPUTS</span></span>

### <span data-ttu-id="e4ca1-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e4ca1-144">System.String</span></span>

### <span data-ttu-id="e4ca1-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="e4ca1-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="e4ca1-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e4ca1-146">OUTPUTS</span></span>

### <span data-ttu-id="e4ca1-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e4ca1-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="e4ca1-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e4ca1-148">NOTES</span></span>

## <span data-ttu-id="e4ca1-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e4ca1-149">RELATED LINKS</span></span>
