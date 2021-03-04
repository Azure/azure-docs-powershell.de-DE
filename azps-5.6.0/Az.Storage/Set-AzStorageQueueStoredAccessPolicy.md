---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: e2e88cc676fddd6da7ce460fbe0d9d770756c4c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929688"
---
# <span data-ttu-id="3701a-101">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3701a-101">Set-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="3701a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3701a-102">SYNOPSIS</span></span>
<span data-ttu-id="3701a-103">Legt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speicherwarteschlange fest.</span><span class="sxs-lookup"><span data-stu-id="3701a-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="3701a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3701a-104">SYNTAX</span></span>

```
Set-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3701a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3701a-105">DESCRIPTION</span></span>
<span data-ttu-id="3701a-106">Das **Cmdlet Set-AzStorageQueueStoredAccessPolicy** legt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speicherwarteschlange fest.</span><span class="sxs-lookup"><span data-stu-id="3701a-106">The **Set-AzStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="3701a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3701a-107">EXAMPLES</span></span>

### <span data-ttu-id="3701a-108">Beispiel 1: Festlegen einer gespeicherten Zugriffsrichtlinie in der Warteschlange mit voller Berechtigung</span><span class="sxs-lookup"><span data-stu-id="3701a-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="3701a-109">Mit diesem Befehl wird eine Zugriffsrichtlinie mit dem Namen "Policy07 für Speicherwarteschlange" mit dem Namen "MyQueue" definiert.</span><span class="sxs-lookup"><span data-stu-id="3701a-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="3701a-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3701a-110">PARAMETERS</span></span>

### <span data-ttu-id="3701a-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3701a-111">-Context</span></span>
<span data-ttu-id="3701a-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="3701a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3701a-113">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3701a-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3701a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3701a-114">-DefaultProfile</span></span>
<span data-ttu-id="3701a-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3701a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3701a-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3701a-116">-ExpiryTime</span></span>
<span data-ttu-id="3701a-117">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="3701a-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3701a-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3701a-118">-NoExpiryTime</span></span>
<span data-ttu-id="3701a-119">Gibt an, dass die Zugriffsrichtlinie kein Ablaufdatum hat.</span><span class="sxs-lookup"><span data-stu-id="3701a-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="3701a-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="3701a-120">-NoStartTime</span></span>
<span data-ttu-id="3701a-121">Gibt an, dass mit diesem Cmdlet die Startzeit auf $Null.</span><span class="sxs-lookup"><span data-stu-id="3701a-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="3701a-122">-Permission</span><span class="sxs-lookup"><span data-stu-id="3701a-122">-Permission</span></span>
<span data-ttu-id="3701a-123">Gibt Berechtigungen in der Richtlinie für gespeicherten Zugriff an, um auf die Speicherwarteschlange zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="3701a-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="3701a-124">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für Lesen, Schreiben und Löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="3701a-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="3701a-125">-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="3701a-125">-Policy</span></span>
<span data-ttu-id="3701a-126">Gibt den Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="3701a-126">Specifies the name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3701a-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="3701a-127">-Queue</span></span>
<span data-ttu-id="3701a-128">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="3701a-128">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3701a-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3701a-129">-StartTime</span></span>
<span data-ttu-id="3701a-130">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="3701a-130">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3701a-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3701a-131">-Confirm</span></span>
<span data-ttu-id="3701a-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3701a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3701a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3701a-133">-WhatIf</span></span>
<span data-ttu-id="3701a-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3701a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3701a-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3701a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3701a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3701a-136">CommonParameters</span></span>
<span data-ttu-id="3701a-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3701a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3701a-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3701a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3701a-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3701a-139">INPUTS</span></span>

### <span data-ttu-id="3701a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3701a-140">System.String</span></span>

### <span data-ttu-id="3701a-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3701a-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3701a-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3701a-142">OUTPUTS</span></span>

### <span data-ttu-id="3701a-143">System.String</span><span class="sxs-lookup"><span data-stu-id="3701a-143">System.String</span></span>

## <span data-ttu-id="3701a-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3701a-144">NOTES</span></span>

## <span data-ttu-id="3701a-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3701a-145">RELATED LINKS</span></span>

[<span data-ttu-id="3701a-146">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3701a-146">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="3701a-147">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3701a-147">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="3701a-148">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3701a-148">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)
