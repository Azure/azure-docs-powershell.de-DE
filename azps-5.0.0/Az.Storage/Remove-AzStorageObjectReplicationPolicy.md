---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 4c42fe6e612f30ab622a0a04498e5474f27690e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176010"
---
# <span data-ttu-id="f5313-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="f5313-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="f5313-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5313-102">SYNOPSIS</span></span>
<span data-ttu-id="f5313-103">Entfernt die angegebene Objekt Replikationsrichtlinie von einem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="f5313-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="f5313-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5313-104">SYNTAX</span></span>

### <span data-ttu-id="f5313-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="f5313-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5313-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="f5313-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5313-107">Richtlinienobject</span><span class="sxs-lookup"><span data-stu-id="f5313-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5313-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5313-108">DESCRIPTION</span></span>
<span data-ttu-id="f5313-109">Das Cmdlet **Remove-AzStorageObjectReplicationPolicy** entfernt die angegebene Objekt Replikationsrichtlinie von einem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="f5313-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="f5313-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5313-110">EXAMPLES</span></span>

### <span data-ttu-id="f5313-111">Beispiel 1: Entfernen einer Objekt Replikationsrichtlinie mit einer bestimmten Richtlinien-Nr von einem Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="f5313-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="f5313-112">Mit diesem Befehl wird eine Objekt Replikationsrichtlinie mit einer bestimmten Richtlinien-Nr von einem Speicherkonto entfernt.</span><span class="sxs-lookup"><span data-stu-id="f5313-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="f5313-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5313-113">PARAMETERS</span></span>

### <span data-ttu-id="f5313-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5313-114">-DefaultProfile</span></span>
<span data-ttu-id="f5313-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5313-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5313-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f5313-116">-InputObject</span></span>
<span data-ttu-id="f5313-117">Objekt Replikationsrichtlinien Objekt, das gelöscht werden soll</span><span class="sxs-lookup"><span data-stu-id="f5313-117">Object Replication Policy object to Delete.</span></span>

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

### <span data-ttu-id="f5313-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5313-118">-PassThru</span></span>
<span data-ttu-id="f5313-119">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="f5313-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f5313-120">-Richtlinien-Nr</span><span class="sxs-lookup"><span data-stu-id="f5313-120">-PolicyId</span></span>
<span data-ttu-id="f5313-121">Objekt Replikationsrichtlinien-ID.</span><span class="sxs-lookup"><span data-stu-id="f5313-121">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="f5313-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5313-122">-ResourceGroupName</span></span>
<span data-ttu-id="f5313-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f5313-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5313-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5313-124">-StorageAccount</span></span>
<span data-ttu-id="f5313-125">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="f5313-125">Storage account object</span></span>

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

### <span data-ttu-id="f5313-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f5313-126">-StorageAccountName</span></span>
<span data-ttu-id="f5313-127">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="f5313-127">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5313-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f5313-128">-Confirm</span></span>
<span data-ttu-id="f5313-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5313-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5313-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5313-130">-WhatIf</span></span>
<span data-ttu-id="f5313-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5313-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5313-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5313-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5313-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5313-133">CommonParameters</span></span>
<span data-ttu-id="f5313-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5313-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5313-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5313-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5313-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5313-136">INPUTS</span></span>

### <span data-ttu-id="f5313-137">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5313-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f5313-138">Microsoft. Azure. Commands. Management. Storage. Models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="f5313-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="f5313-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5313-139">OUTPUTS</span></span>

### <span data-ttu-id="f5313-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5313-140">System.Boolean</span></span>

## <span data-ttu-id="f5313-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5313-141">NOTES</span></span>

## <span data-ttu-id="f5313-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5313-142">RELATED LINKS</span></span>
