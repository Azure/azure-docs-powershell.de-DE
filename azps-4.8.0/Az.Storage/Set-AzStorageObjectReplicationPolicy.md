---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: bf8d7aade5eeeafc2c3a78e4cdfed5df2d733006
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166756"
---
# <span data-ttu-id="b8c78-101">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="b8c78-101">Set-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="b8c78-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b8c78-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c78-103">Erstellt oder aktualisiert die angegebene Objekt Replikationsrichtlinie in einem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="b8c78-103">Creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="b8c78-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8c78-104">SYNTAX</span></span>

### <span data-ttu-id="b8c78-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="b8c78-105">AccountName (Default)</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] -SourceAccount <String> [-DestinationAccount <String>]
 -Rule <PSObjectReplicationPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8c78-106">Richtlinienobject</span><span class="sxs-lookup"><span data-stu-id="b8c78-106">PolicyObject</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -InputObject <PSObjectReplicationPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8c78-107">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="b8c78-107">AccountObject</span></span>
```
Set-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 -SourceAccount <String> [-DestinationAccount <String>] -Rule <PSObjectReplicationPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8c78-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8c78-108">DESCRIPTION</span></span>
<span data-ttu-id="b8c78-109">Das Cmdlet " **festlegen-AzStorageObjectReplicationPolicy** " erstellt oder aktualisiert die angegebene Objekt Replikationsrichtlinie in einem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="b8c78-109">The **Set-AzStorageObjectReplicationPolicy** cmdlet creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="b8c78-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b8c78-110">EXAMPLES</span></span>

### <span data-ttu-id="b8c78-111">Beispiel 1: Festlegen von Objekt Replikationsrichtlinien auf Ziel-und Quellkonto</span><span class="sxs-lookup"><span data-stu-id="b8c78-111">Example 1: Set object replication policy to both destination and source account.</span></span>
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

<span data-ttu-id="b8c78-112">Dieser Befehl legt die Objekt Replikationsrichtlinie auf das Ziel-und das Quellkonto fest.</span><span class="sxs-lookup"><span data-stu-id="b8c78-112">This command sets object replication policy to both destination and source account.</span></span>
<span data-ttu-id="b8c78-113">Erstellen Sie zunächst zwei Richtlinien Regeln für die Objektreplikation, und legen Sie die Richtlinie mit dem Konto 2 Regeln für Ziel fest.</span><span class="sxs-lookup"><span data-stu-id="b8c78-113">First create 2 object replication policy rules, and set policy with the 2 rules to destination account.</span></span> <span data-ttu-id="b8c78-114">Legen Sie dann die Objekt Replikationsrichtlinie vom Zielkonto auf Quellkonto ab.</span><span class="sxs-lookup"><span data-stu-id="b8c78-114">Then set the object replication policy from destination account to source account.</span></span>

## <span data-ttu-id="b8c78-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8c78-115">PARAMETERS</span></span>

### <span data-ttu-id="b8c78-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c78-116">-DefaultProfile</span></span>
<span data-ttu-id="b8c78-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b8c78-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8c78-118">-DestinationAccount</span><span class="sxs-lookup"><span data-stu-id="b8c78-118">-DestinationAccount</span></span>
<span data-ttu-id="b8c78-119">Objekt Replikationsrichtlinien DestinationAccount</span><span class="sxs-lookup"><span data-stu-id="b8c78-119">Object Replication Policy DestinationAccount.</span></span>

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

### <span data-ttu-id="b8c78-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b8c78-120">-InputObject</span></span>
<span data-ttu-id="b8c78-121">Objekt Replikationsrichtlinien Objekt, das auf das angegebene Konto festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8c78-121">Object Replication Policy Object to Set to the specified Account.</span></span>

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

### <span data-ttu-id="b8c78-122">-Richtlinien-Nr</span><span class="sxs-lookup"><span data-stu-id="b8c78-122">-PolicyId</span></span>
<span data-ttu-id="b8c78-123">Objekt Replikationsrichtlinien-ID. Es sollte eine GUID oder "Default" sein.</span><span class="sxs-lookup"><span data-stu-id="b8c78-123">Object Replication Policy Id. It should be a GUID or 'default'.</span></span>
<span data-ttu-id="b8c78-124">Wenn die Richtlinien-ID nicht eingegeben wird, wird "Standard" verwendet, was bedeutet, dass eine neue Richtlinie erstellt und die ID der neuen Richtlinie in der erstellten Richtlinie zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b8c78-124">If not input the PolicyId, will use 'default', which means to create a new policy and the Id of the new policy will be returned in the created policy.</span></span>

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

### <span data-ttu-id="b8c78-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c78-125">-ResourceGroupName</span></span>
<span data-ttu-id="b8c78-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b8c78-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="b8c78-127">-Rule</span><span class="sxs-lookup"><span data-stu-id="b8c78-127">-Rule</span></span>
<span data-ttu-id="b8c78-128">Regeln für Objekt Replikationsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="b8c78-128">Object Replication Policy Rules.</span></span>

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

### <span data-ttu-id="b8c78-129">-SourceAccount</span><span class="sxs-lookup"><span data-stu-id="b8c78-129">-SourceAccount</span></span>
<span data-ttu-id="b8c78-130">Objekt Replikationsrichtlinien SourceAccount</span><span class="sxs-lookup"><span data-stu-id="b8c78-130">Object Replication Policy SourceAccount.</span></span>

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

### <span data-ttu-id="b8c78-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b8c78-131">-StorageAccount</span></span>
<span data-ttu-id="b8c78-132">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="b8c78-132">Storage account object</span></span>

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

### <span data-ttu-id="b8c78-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b8c78-133">-StorageAccountName</span></span>
<span data-ttu-id="b8c78-134">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="b8c78-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="b8c78-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b8c78-135">-Confirm</span></span>
<span data-ttu-id="b8c78-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8c78-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8c78-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8c78-137">-WhatIf</span></span>
<span data-ttu-id="b8c78-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8c78-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8c78-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8c78-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8c78-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c78-140">CommonParameters</span></span>
<span data-ttu-id="b8c78-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8c78-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c78-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8c78-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c78-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b8c78-143">INPUTS</span></span>

### <span data-ttu-id="b8c78-144">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b8c78-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b8c78-145">Microsoft. Azure. Commands. Management. Storage. Models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="b8c78-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="b8c78-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b8c78-146">OUTPUTS</span></span>

### <span data-ttu-id="b8c78-147">Microsoft. Azure. Commands. Management. Storage. Models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="b8c78-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="b8c78-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="b8c78-148">NOTES</span></span>

## <span data-ttu-id="b8c78-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b8c78-149">RELATED LINKS</span></span>
