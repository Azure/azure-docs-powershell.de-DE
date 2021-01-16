---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 822781f6c46eeb76a953eaa66935c03cd76df737
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289901"
---
# <span data-ttu-id="c75ab-101">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c75ab-101">Set-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="c75ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c75ab-102">SYNOPSIS</span></span>
<span data-ttu-id="c75ab-103">Legt die Richtlinie für den gespeicherten Zugriff für eine Azure -Speichertabelle fest.</span><span class="sxs-lookup"><span data-stu-id="c75ab-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="c75ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c75ab-104">SYNTAX</span></span>

```
Set-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c75ab-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c75ab-105">DESCRIPTION</span></span>
<span data-ttu-id="c75ab-106">Das **Cmdlet "Set-AzStorageTableStoredAccessPolicy"** hat die gespeicherte Zugriffsrichtlinie für eine Azure -Speichertabelle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c75ab-106">The **Set-AzStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="c75ab-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c75ab-107">EXAMPLES</span></span>

### <span data-ttu-id="c75ab-108">Beispiel 1: Festlegen einer gespeicherten Zugriffsrichtlinie in einer Tabelle mit der vollen Berechtigung</span><span class="sxs-lookup"><span data-stu-id="c75ab-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="c75ab-109">Mit diesem Befehl wird eine Zugriffsrichtlinie mit dem Namen "Policy08" für die Speichertabelle namens "MyTable" definiert.</span><span class="sxs-lookup"><span data-stu-id="c75ab-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="c75ab-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c75ab-110">PARAMETERS</span></span>

### <span data-ttu-id="c75ab-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c75ab-111">-Context</span></span>
<span data-ttu-id="c75ab-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="c75ab-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c75ab-113">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c75ab-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c75ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c75ab-114">-DefaultProfile</span></span>
<span data-ttu-id="c75ab-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c75ab-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c75ab-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c75ab-116">-ExpiryTime</span></span>
<span data-ttu-id="c75ab-117">Gibt den Zeitpunkt an, zu dem die Richtlinie für den gespeicherten Zugriff abläuft.</span><span class="sxs-lookup"><span data-stu-id="c75ab-117">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="c75ab-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c75ab-118">-NoExpiryTime</span></span>
<span data-ttu-id="c75ab-119">Gibt an, dass die Zugriffsrichtlinie kein Ablaufdatum hat.</span><span class="sxs-lookup"><span data-stu-id="c75ab-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="c75ab-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="c75ab-120">-NoStartTime</span></span>
<span data-ttu-id="c75ab-121">Gibt an, dass die Startzeit auf "$Null" festgelegt $Null.</span><span class="sxs-lookup"><span data-stu-id="c75ab-121">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="c75ab-122">-Permission</span><span class="sxs-lookup"><span data-stu-id="c75ab-122">-Permission</span></span>
<span data-ttu-id="c75ab-123">Gibt Berechtigungen in der Richtlinie für den gespeicherten Zugriff für den Zugriff auf die Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="c75ab-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="c75ab-124">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` "Lesen", "Schreiben" und "Löschen" handelt.</span><span class="sxs-lookup"><span data-stu-id="c75ab-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="c75ab-125">-Policy</span><span class="sxs-lookup"><span data-stu-id="c75ab-125">-Policy</span></span>
<span data-ttu-id="c75ab-126">Gibt den Namen der gespeicherten Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="c75ab-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="c75ab-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c75ab-127">-StartTime</span></span>
<span data-ttu-id="c75ab-128">Gibt den Zeitpunkt an, zu dem die Gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="c75ab-128">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="c75ab-129">-Table</span><span class="sxs-lookup"><span data-stu-id="c75ab-129">-Table</span></span>
<span data-ttu-id="c75ab-130">Gibt den Namen der Azure -Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="c75ab-130">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="c75ab-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c75ab-131">-Confirm</span></span>
<span data-ttu-id="c75ab-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c75ab-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c75ab-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c75ab-133">-WhatIf</span></span>
<span data-ttu-id="c75ab-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c75ab-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c75ab-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c75ab-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c75ab-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c75ab-136">CommonParameters</span></span>
<span data-ttu-id="c75ab-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c75ab-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c75ab-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c75ab-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c75ab-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c75ab-139">INPUTS</span></span>

### <span data-ttu-id="c75ab-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c75ab-140">System.String</span></span>

### <span data-ttu-id="c75ab-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c75ab-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c75ab-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c75ab-142">OUTPUTS</span></span>

### <span data-ttu-id="c75ab-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c75ab-143">System.String</span></span>

## <span data-ttu-id="c75ab-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c75ab-144">NOTES</span></span>

## <span data-ttu-id="c75ab-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c75ab-145">RELATED LINKS</span></span>

[<span data-ttu-id="c75ab-146">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c75ab-146">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="c75ab-147">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c75ab-147">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="c75ab-148">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c75ab-148">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="c75ab-149">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c75ab-149">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)
