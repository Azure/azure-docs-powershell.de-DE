---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 4c42fe6e612f30ab622a0a04498e5474f27690e9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460211"
---
# <span data-ttu-id="63a64-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="63a64-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="63a64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63a64-102">SYNOPSIS</span></span>
<span data-ttu-id="63a64-103">Entfernt die angegebene Objektreplikationsrichtlinie aus einem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="63a64-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="63a64-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63a64-104">SYNTAX</span></span>

### <span data-ttu-id="63a64-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="63a64-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63a64-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="63a64-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63a64-107">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="63a64-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63a64-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63a64-108">DESCRIPTION</span></span>
<span data-ttu-id="63a64-109">Das **Cmdlet "Remove-AzStorageObjectReplicationPolicy"** entfernt die angegebene Objektreplikationsrichtlinie aus einem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="63a64-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="63a64-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="63a64-110">EXAMPLES</span></span>

### <span data-ttu-id="63a64-111">Beispiel 1: Entfernen einer Objektreplikationsrichtlinie mit einer bestimmten policyId aus einem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="63a64-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="63a64-112">Mit diesem Befehl wird eine Objektreplikationsrichtlinie mit einer bestimmten policyId aus einem Speicherkonto entfernt.</span><span class="sxs-lookup"><span data-stu-id="63a64-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="63a64-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63a64-113">PARAMETERS</span></span>

### <span data-ttu-id="63a64-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63a64-114">-DefaultProfile</span></span>
<span data-ttu-id="63a64-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63a64-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63a64-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63a64-116">-InputObject</span></span>
<span data-ttu-id="63a64-117">Objektreplikationsrichtlinienobjekt zum Löschen</span><span class="sxs-lookup"><span data-stu-id="63a64-117">Object Replication Policy object to Delete.</span></span>

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

### <span data-ttu-id="63a64-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63a64-118">-PassThru</span></span>
<span data-ttu-id="63a64-119">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="63a64-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="63a64-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="63a64-120">-PolicyId</span></span>
<span data-ttu-id="63a64-121">Id der Objektreplikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="63a64-121">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="63a64-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63a64-122">-ResourceGroupName</span></span>
<span data-ttu-id="63a64-123">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="63a64-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="63a64-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="63a64-124">-StorageAccount</span></span>
<span data-ttu-id="63a64-125">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="63a64-125">Storage account object</span></span>

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

### <span data-ttu-id="63a64-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="63a64-126">-StorageAccountName</span></span>
<span data-ttu-id="63a64-127">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="63a64-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="63a64-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63a64-128">-Confirm</span></span>
<span data-ttu-id="63a64-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="63a64-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63a64-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="63a64-130">-WhatIf</span></span>
<span data-ttu-id="63a64-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="63a64-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63a64-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63a64-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63a64-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63a64-133">CommonParameters</span></span>
<span data-ttu-id="63a64-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63a64-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63a64-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63a64-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63a64-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="63a64-136">INPUTS</span></span>

### <span data-ttu-id="63a64-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="63a64-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="63a64-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="63a64-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="63a64-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="63a64-139">OUTPUTS</span></span>

### <span data-ttu-id="63a64-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="63a64-140">System.Boolean</span></span>

## <span data-ttu-id="63a64-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="63a64-141">NOTES</span></span>

## <span data-ttu-id="63a64-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="63a64-142">RELATED LINKS</span></span>
