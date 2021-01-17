---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: be0e79bbc6d1cd9c2a356852e2d9dea83439d25f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468339"
---
# <span data-ttu-id="3c899-101">New-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="3c899-101">New-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="3c899-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c899-102">SYNOPSIS</span></span>
<span data-ttu-id="3c899-103">Schlüssel des Remoterenderingkontos erneut erstellen</span><span class="sxs-lookup"><span data-stu-id="3c899-103">Regenerate key of Remote Rendering Account</span></span>

## <span data-ttu-id="3c899-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c899-104">SYNTAX</span></span>

### <span data-ttu-id="3c899-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c899-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c899-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c899-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c899-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c899-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c899-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c899-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c899-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c899-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c899-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c899-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c899-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c899-111">DESCRIPTION</span></span>
<span data-ttu-id="3c899-112">Erstellen Sie den Primärschlüssel oder sekundären Schlüssel des Remoterenderingkontos erneut.</span><span class="sxs-lookup"><span data-stu-id="3c899-112">Regenerate primary key or secondary key of Remote Rendering Account.</span></span>

## <span data-ttu-id="3c899-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3c899-113">EXAMPLES</span></span>

### <span data-ttu-id="3c899-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3c899-114">Example 1</span></span>
```powershell
PS C:\> New-AzRemoteRenderingAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="3c899-115">Erstellen Sie den sekundären Schlüssel des Remoterenderingkontos erneut als "Beispiel" in der Ressourcengruppe "rg1".</span><span class="sxs-lookup"><span data-stu-id="3c899-115">Regenerate secondary key of Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="3c899-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3c899-116">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | New-AzRemoteRenderingAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="3c899-117">Erstellen Sie den sekundären Schlüssel des Remoterenderingkontos "example" erneut aus der aktuellen Abonnement- und Ressourcengruppe "rg1" mit Piping.</span><span class="sxs-lookup"><span data-stu-id="3c899-117">Regenerate secondary key of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="3c899-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c899-118">PARAMETERS</span></span>

### <span data-ttu-id="3c899-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c899-119">-DefaultProfile</span></span>
<span data-ttu-id="3c899-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3c899-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c899-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3c899-121">-Force</span></span>
<span data-ttu-id="3c899-122">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="3c899-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3c899-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c899-123">-InputObject</span></span>
<span data-ttu-id="3c899-124">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="3c899-124">The custom domain object.</span></span>

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

### <span data-ttu-id="3c899-125">-Name</span><span class="sxs-lookup"><span data-stu-id="3c899-125">-Name</span></span>
<span data-ttu-id="3c899-126">Kontoname des Remoterenderings.</span><span class="sxs-lookup"><span data-stu-id="3c899-126">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="3c899-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="3c899-127">-Primary</span></span>
<span data-ttu-id="3c899-128">Erstellen Sie den Primärschlüssel des Remoterenderkontos erneut.</span><span class="sxs-lookup"><span data-stu-id="3c899-128">Regenerate primary key of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="3c899-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c899-129">-ResourceGroupName</span></span>
<span data-ttu-id="3c899-130">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="3c899-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="3c899-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c899-131">-ResourceId</span></span>
<span data-ttu-id="3c899-132">Ressourcen-ID des Remoterenderingkontos.</span><span class="sxs-lookup"><span data-stu-id="3c899-132">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="3c899-133">-Secondary</span><span class="sxs-lookup"><span data-stu-id="3c899-133">-Secondary</span></span>
<span data-ttu-id="3c899-134">Erstellen Sie den Primärschlüssel des Remoterenderkontos erneut.</span><span class="sxs-lookup"><span data-stu-id="3c899-134">Regenerate primary key of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="3c899-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c899-135">-Confirm</span></span>
<span data-ttu-id="3c899-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c899-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c899-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3c899-137">-WhatIf</span></span>
<span data-ttu-id="3c899-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c899-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c899-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3c899-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c899-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c899-140">CommonParameters</span></span>
<span data-ttu-id="3c899-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c899-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3c899-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c899-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c899-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3c899-143">INPUTS</span></span>

### <span data-ttu-id="3c899-144">System.String</span><span class="sxs-lookup"><span data-stu-id="3c899-144">System.String</span></span>

### <span data-ttu-id="3c899-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="3c899-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="3c899-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3c899-146">OUTPUTS</span></span>

### <span data-ttu-id="3c899-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3c899-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="3c899-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3c899-148">NOTES</span></span>

## <span data-ttu-id="3c899-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3c899-149">RELATED LINKS</span></span>
