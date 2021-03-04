---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 17ccb6e41e826ffd6b522c353ff51cf360b5af0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923275"
---
# <span data-ttu-id="d5b5d-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="d5b5d-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="d5b5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5b5d-102">SYNOPSIS</span></span>
<span data-ttu-id="d5b5d-103">Entfernt die angegebene Objektreplikationsrichtlinie aus einem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="d5b5d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5b5d-104">SYNTAX</span></span>

### <span data-ttu-id="d5b5d-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5b5d-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5b5d-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d5b5d-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5b5d-107">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="d5b5d-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5b5d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5b5d-108">DESCRIPTION</span></span>
<span data-ttu-id="d5b5d-109">Das **Cmdlet Remove-AzStorageObjectReplicationPolicy** entfernt die angegebene Objektreplikationsrichtlinie aus einem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="d5b5d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d5b5d-110">EXAMPLES</span></span>

### <span data-ttu-id="d5b5d-111">Beispiel 1: Entfernen einer Objektreplikationsrichtlinie mit einer bestimmten policyId aus einem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="d5b5d-112">Mit diesem Befehl wird eine Objektreplikationsrichtlinie mit einer bestimmten policyId aus einem Speicherkonto entfernt.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="d5b5d-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d5b5d-113">PARAMETERS</span></span>

### <span data-ttu-id="d5b5d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5b5d-114">-DefaultProfile</span></span>
<span data-ttu-id="d5b5d-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5b5d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5b5d-116">-InputObject</span></span>
<span data-ttu-id="d5b5d-117">Objektreplikationsrichtlinienobjekt zu Löschen.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-117">Object Replication Policy object to Delete.</span></span>

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

### <span data-ttu-id="d5b5d-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5b5d-118">-PassThru</span></span>
<span data-ttu-id="d5b5d-119">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d5b5d-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d5b5d-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="d5b5d-120">-PolicyId</span></span>
<span data-ttu-id="d5b5d-121">Objektreplikationsrichtlinien-ID.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-121">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="d5b5d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5b5d-122">-ResourceGroupName</span></span>
<span data-ttu-id="d5b5d-123">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="d5b5d-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d5b5d-124">-StorageAccount</span></span>
<span data-ttu-id="d5b5d-125">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="d5b5d-125">Storage account object</span></span>

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

### <span data-ttu-id="d5b5d-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d5b5d-126">-StorageAccountName</span></span>
<span data-ttu-id="d5b5d-127">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="d5b5d-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d5b5d-128">-Confirm</span></span>
<span data-ttu-id="d5b5d-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5b5d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5b5d-130">-WhatIf</span></span>
<span data-ttu-id="d5b5d-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5b5d-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5b5d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5b5d-133">CommonParameters</span></span>
<span data-ttu-id="d5b5d-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5b5d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5b5d-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5b5d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5b5d-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d5b5d-136">INPUTS</span></span>

### <span data-ttu-id="d5b5d-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d5b5d-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d5b5d-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="d5b5d-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="d5b5d-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d5b5d-139">OUTPUTS</span></span>

### <span data-ttu-id="d5b5d-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d5b5d-140">System.Boolean</span></span>

## <span data-ttu-id="d5b5d-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d5b5d-141">NOTES</span></span>

## <span data-ttu-id="d5b5d-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d5b5d-142">RELATED LINKS</span></span>
