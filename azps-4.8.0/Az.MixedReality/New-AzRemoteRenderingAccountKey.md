---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: be0e79bbc6d1cd9c2a356852e2d9dea83439d25f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173703"
---
# <span data-ttu-id="0fe54-101">New-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="0fe54-101">New-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="0fe54-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0fe54-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe54-103">Schlüssel des Remote Rendering-Kontos erneut generieren</span><span class="sxs-lookup"><span data-stu-id="0fe54-103">Regenerate key of Remote Rendering Account</span></span>

## <span data-ttu-id="0fe54-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fe54-104">SYNTAX</span></span>

### <span data-ttu-id="0fe54-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fe54-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fe54-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fe54-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fe54-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fe54-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fe54-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fe54-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fe54-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fe54-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fe54-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fe54-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fe54-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fe54-111">DESCRIPTION</span></span>
<span data-ttu-id="0fe54-112">Neugenerieren des Primärschlüssels oder des sekundären Schlüssels des Remote Rendering-Kontos</span><span class="sxs-lookup"><span data-stu-id="0fe54-112">Regenerate primary key or secondary key of Remote Rendering Account.</span></span>

## <span data-ttu-id="0fe54-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0fe54-113">EXAMPLES</span></span>

### <span data-ttu-id="0fe54-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0fe54-114">Example 1</span></span>
```powershell
PS C:\> New-AzRemoteRenderingAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="0fe54-115">Sekundärer Schlüssel des Remote Rendering-Kontos erneut generieren "Beispiel" in der Ressourcengruppe "RG1".</span><span class="sxs-lookup"><span data-stu-id="0fe54-115">Regenerate secondary key of Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="0fe54-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0fe54-116">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | New-AzRemoteRenderingAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="0fe54-117">Sekundärer Schlüssel des Remote Rendering-Kontos erneut generieren "Beispiel" aus dem aktuellen Abonnement und der Ressourcengruppe "RG1" mit Piping.</span><span class="sxs-lookup"><span data-stu-id="0fe54-117">Regenerate secondary key of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="0fe54-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fe54-118">PARAMETERS</span></span>

### <span data-ttu-id="0fe54-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe54-119">-DefaultProfile</span></span>
<span data-ttu-id="0fe54-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0fe54-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fe54-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0fe54-121">-Force</span></span>
<span data-ttu-id="0fe54-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="0fe54-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0fe54-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0fe54-123">-InputObject</span></span>
<span data-ttu-id="0fe54-124">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="0fe54-124">The custom domain object.</span></span>

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

### <span data-ttu-id="0fe54-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0fe54-125">-Name</span></span>
<span data-ttu-id="0fe54-126">Name des Remote Rendering-Kontos</span><span class="sxs-lookup"><span data-stu-id="0fe54-126">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="0fe54-127">– Primär</span><span class="sxs-lookup"><span data-stu-id="0fe54-127">-Primary</span></span>
<span data-ttu-id="0fe54-128">Primärschlüssel des Remote Rendering-Kontos erneut generieren</span><span class="sxs-lookup"><span data-stu-id="0fe54-128">Regenerate primary key of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="0fe54-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fe54-129">-ResourceGroupName</span></span>
<span data-ttu-id="0fe54-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0fe54-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="0fe54-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0fe54-131">-ResourceId</span></span>
<span data-ttu-id="0fe54-132">Ressourcen-ID des Remote Rendering-Kontos.</span><span class="sxs-lookup"><span data-stu-id="0fe54-132">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="0fe54-133">-Sekundäre</span><span class="sxs-lookup"><span data-stu-id="0fe54-133">-Secondary</span></span>
<span data-ttu-id="0fe54-134">Primärschlüssel des Remote Rendering-Kontos erneut generieren</span><span class="sxs-lookup"><span data-stu-id="0fe54-134">Regenerate primary key of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="0fe54-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0fe54-135">-Confirm</span></span>
<span data-ttu-id="0fe54-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0fe54-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fe54-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fe54-137">-WhatIf</span></span>
<span data-ttu-id="0fe54-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fe54-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0fe54-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0fe54-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fe54-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe54-140">CommonParameters</span></span>
<span data-ttu-id="0fe54-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fe54-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0fe54-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fe54-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe54-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0fe54-143">INPUTS</span></span>

### <span data-ttu-id="0fe54-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0fe54-144">System.String</span></span>

### <span data-ttu-id="0fe54-145">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="0fe54-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="0fe54-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0fe54-146">OUTPUTS</span></span>

### <span data-ttu-id="0fe54-147">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0fe54-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="0fe54-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="0fe54-148">NOTES</span></span>

## <span data-ttu-id="0fe54-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0fe54-149">RELATED LINKS</span></span>
