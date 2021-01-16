---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 0f8d9860f04112c197b91907a7622683069c3589
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376114"
---
# <span data-ttu-id="f72e3-101">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f72e3-101">Set-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="f72e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f72e3-102">SYNOPSIS</span></span>
<span data-ttu-id="f72e3-103">Legt eine Richtlinie für den gespeicherten Zugriff für eine Azure-Speicherwarteschlange fest.</span><span class="sxs-lookup"><span data-stu-id="f72e3-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="f72e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f72e3-104">SYNTAX</span></span>

```
Set-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f72e3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f72e3-105">DESCRIPTION</span></span>
<span data-ttu-id="f72e3-106">Das **Cmdlet "Set-AzStorageQueueStoredAccessPolicy"** legt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speicherwarteschlange fest.</span><span class="sxs-lookup"><span data-stu-id="f72e3-106">The **Set-AzStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="f72e3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f72e3-107">EXAMPLES</span></span>

### <span data-ttu-id="f72e3-108">Beispiel 1: Festlegen einer gespeicherten Zugriffsrichtlinie in der Warteschlange mit der vollen Berechtigung</span><span class="sxs-lookup"><span data-stu-id="f72e3-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="f72e3-109">Mit diesem Befehl wird eine Zugriffsrichtlinie namens "Policy07" für die Speicherwarteschlange namens "MyQueue" definiert.</span><span class="sxs-lookup"><span data-stu-id="f72e3-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="f72e3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f72e3-110">PARAMETERS</span></span>

### <span data-ttu-id="f72e3-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f72e3-111">-Context</span></span>
<span data-ttu-id="f72e3-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="f72e3-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f72e3-113">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f72e3-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f72e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f72e3-114">-DefaultProfile</span></span>
<span data-ttu-id="f72e3-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f72e3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f72e3-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f72e3-116">-ExpiryTime</span></span>
<span data-ttu-id="f72e3-117">Gibt den Zeitpunkt an, zu dem die Richtlinie für den gespeicherten Zugriff ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="f72e3-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="f72e3-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f72e3-118">-NoExpiryTime</span></span>
<span data-ttu-id="f72e3-119">Gibt an, dass die Zugriffsrichtlinie kein Ablaufdatum hat.</span><span class="sxs-lookup"><span data-stu-id="f72e3-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="f72e3-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="f72e3-120">-NoStartTime</span></span>
<span data-ttu-id="f72e3-121">Zeigt an, dass für dieses Cmdlet die Startzeit auf $Null.</span><span class="sxs-lookup"><span data-stu-id="f72e3-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="f72e3-122">-Permission</span><span class="sxs-lookup"><span data-stu-id="f72e3-122">-Permission</span></span>
<span data-ttu-id="f72e3-123">Gibt Berechtigungen in der Richtlinie für gespeicherten Zugriff für den Zugriff auf die Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="f72e3-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="f72e3-124">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` "Lesen", "Schreiben" und "Löschen" handelt.</span><span class="sxs-lookup"><span data-stu-id="f72e3-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="f72e3-125">-Policy</span><span class="sxs-lookup"><span data-stu-id="f72e3-125">-Policy</span></span>
<span data-ttu-id="f72e3-126">Gibt den Namen der gespeicherten Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="f72e3-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="f72e3-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="f72e3-127">-Queue</span></span>
<span data-ttu-id="f72e3-128">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="f72e3-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="f72e3-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f72e3-129">-StartTime</span></span>
<span data-ttu-id="f72e3-130">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="f72e3-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="f72e3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f72e3-131">-Confirm</span></span>
<span data-ttu-id="f72e3-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f72e3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f72e3-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f72e3-133">-WhatIf</span></span>
<span data-ttu-id="f72e3-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f72e3-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f72e3-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f72e3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f72e3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f72e3-136">CommonParameters</span></span>
<span data-ttu-id="f72e3-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f72e3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f72e3-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f72e3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f72e3-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f72e3-139">INPUTS</span></span>

### <span data-ttu-id="f72e3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f72e3-140">System.String</span></span>

### <span data-ttu-id="f72e3-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f72e3-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f72e3-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f72e3-142">OUTPUTS</span></span>

### <span data-ttu-id="f72e3-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f72e3-143">System.String</span></span>

## <span data-ttu-id="f72e3-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f72e3-144">NOTES</span></span>

## <span data-ttu-id="f72e3-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f72e3-145">RELATED LINKS</span></span>

[<span data-ttu-id="f72e3-146">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f72e3-146">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="f72e3-147">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f72e3-147">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="f72e3-148">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f72e3-148">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)
