---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: bf8d7aade5eeeafc2c3a78e4cdfed5df2d733006
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173676"
---
# <span data-ttu-id="d9734-101">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="d9734-101">Set-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="d9734-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9734-102">SYNOPSIS</span></span>
<span data-ttu-id="d9734-103">Erstellt oder aktualisiert die angegebene Objektreplikationsrichtlinie in einem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="d9734-103">Creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="d9734-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9734-104">SYNTAX</span></span>

### <span data-ttu-id="d9734-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d9734-105">AccountName (Default)</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] -SourceAccount <String> [-DestinationAccount <String>]
 -Rule <PSObjectReplicationPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9734-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="d9734-106">PolicyObject</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -InputObject <PSObjectReplicationPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9734-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d9734-107">AccountObject</span></span>
```
Set-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 -SourceAccount <String> [-DestinationAccount <String>] -Rule <PSObjectReplicationPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9734-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9734-108">DESCRIPTION</span></span>
<span data-ttu-id="d9734-109">Das **Cmdlet "Set-AzStorageObjectReplicationPolicy"** erstellt oder aktualisiert die angegebene Objektreplikationsrichtlinie in einem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="d9734-109">The **Set-AzStorageObjectReplicationPolicy** cmdlet creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="d9734-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d9734-110">EXAMPLES</span></span>

### <span data-ttu-id="d9734-111">Beispiel 1: Festlegen der Objektreplikationsrichtlinie auf Ziel- und Quellkonto.</span><span class="sxs-lookup"><span data-stu-id="d9734-111">Example 1: Set object replication policy to both destination and source account.</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $destPolicy = Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId default -SourceAccount $srcAccountName  -Rule $rule1,$rule2

PS C:\> $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mysourceaccount" -InputObject $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----                                     
myresourcegroup   mysourceaccount    56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
```

<span data-ttu-id="d9734-112">Dieser Befehl legt die Objektreplikationsrichtlinie auf Ziel- und Quellkonto fest.</span><span class="sxs-lookup"><span data-stu-id="d9734-112">This command sets object replication policy to both destination and source account.</span></span>
<span data-ttu-id="d9734-113">Erstellen Sie zuerst zwei Richtlinienregeln für die Objektreplikation, und legen Sie die Richtlinie mit den beiden Regeln für das Zielkonto festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d9734-113">First create 2 object replication policy rules, and set policy with the 2 rules to destination account.</span></span> <span data-ttu-id="d9734-114">Legen Sie dann die Objektreplikationsrichtlinie vom Zielkonto auf das Quellkonto festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d9734-114">Then set the object replication policy from destination account to source account.</span></span>

## <span data-ttu-id="d9734-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9734-115">PARAMETERS</span></span>

### <span data-ttu-id="d9734-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9734-116">-DefaultProfile</span></span>
<span data-ttu-id="d9734-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9734-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9734-118">-DestinationAccount</span><span class="sxs-lookup"><span data-stu-id="d9734-118">-DestinationAccount</span></span>
<span data-ttu-id="d9734-119">DestinationAccount der Objektreplikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="d9734-119">Object Replication Policy DestinationAccount.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9734-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9734-120">-InputObject</span></span>
<span data-ttu-id="d9734-121">Objektreplikationsrichtlinienobjekt, das auf das angegebene Konto festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9734-121">Object Replication Policy Object to Set to the specified Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9734-122">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="d9734-122">-PolicyId</span></span>
<span data-ttu-id="d9734-123">Id der Objektreplikationsrichtlinie. Es sollte eine GUID oder "Standard" sein.</span><span class="sxs-lookup"><span data-stu-id="d9734-123">Object Replication Policy Id. It should be a GUID or 'default'.</span></span>
<span data-ttu-id="d9734-124">Wenn Sie die PolicyId nicht eingeben, wird "default" verwendet, d. h., sie erstellt eine neue Richtlinie, und die ID der neuen Richtlinie wird in der erstellten Richtlinie zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d9734-124">If not input the PolicyId, will use 'default', which means to create a new policy and the Id of the new policy will be returned in the created policy.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9734-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9734-125">-ResourceGroupName</span></span>
<span data-ttu-id="d9734-126">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="d9734-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9734-127">-Rule</span><span class="sxs-lookup"><span data-stu-id="d9734-127">-Rule</span></span>
<span data-ttu-id="d9734-128">Richtlinienregeln für objektreplikation.</span><span class="sxs-lookup"><span data-stu-id="d9734-128">Object Replication Policy Rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule[]
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9734-129">-SourceAccount</span><span class="sxs-lookup"><span data-stu-id="d9734-129">-SourceAccount</span></span>
<span data-ttu-id="d9734-130">SourceAccount der Objektreplikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="d9734-130">Object Replication Policy SourceAccount.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9734-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d9734-131">-StorageAccount</span></span>
<span data-ttu-id="d9734-132">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="d9734-132">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9734-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d9734-133">-StorageAccountName</span></span>
<span data-ttu-id="d9734-134">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="d9734-134">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9734-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9734-135">-Confirm</span></span>
<span data-ttu-id="d9734-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9734-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9734-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d9734-137">-WhatIf</span></span>
<span data-ttu-id="d9734-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9734-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9734-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9734-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9734-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9734-140">CommonParameters</span></span>
<span data-ttu-id="d9734-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9734-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9734-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9734-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9734-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d9734-143">INPUTS</span></span>

### <span data-ttu-id="d9734-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d9734-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d9734-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="d9734-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="d9734-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d9734-146">OUTPUTS</span></span>

### <span data-ttu-id="d9734-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="d9734-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="d9734-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d9734-148">NOTES</span></span>

## <span data-ttu-id="d9734-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d9734-149">RELATED LINKS</span></span>
