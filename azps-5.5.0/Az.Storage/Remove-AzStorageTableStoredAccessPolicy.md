---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 9df25558c752b47e41bf76f7db128bd127ad0c53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157969"
---
# <span data-ttu-id="24016-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="24016-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="24016-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24016-102">SYNOPSIS</span></span>
<span data-ttu-id="24016-103">Entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="24016-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="24016-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24016-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24016-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="24016-105">DESCRIPTION</span></span>
<span data-ttu-id="24016-106">Das **Cmdlet "Remove-AzStorageTableStoredAccessPolicy"** entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="24016-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="24016-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="24016-107">EXAMPLES</span></span>

### <span data-ttu-id="24016-108">Beispiel 1: Entfernen einer gespeicherten Zugriffsrichtlinie aus einer Speichertabelle</span><span class="sxs-lookup"><span data-stu-id="24016-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="24016-109">Mit diesem Befehl wird die Richtlinie mit dem Namen "Policy05" aus der Speichertabelle "MyTable" entfernt.</span><span class="sxs-lookup"><span data-stu-id="24016-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="24016-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24016-110">PARAMETERS</span></span>

### <span data-ttu-id="24016-111">-Context</span><span class="sxs-lookup"><span data-stu-id="24016-111">-Context</span></span>
<span data-ttu-id="24016-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="24016-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="24016-113">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24016-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="24016-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24016-114">-DefaultProfile</span></span>
<span data-ttu-id="24016-115">Kommunikation mit Azure.</span><span class="sxs-lookup"><span data-stu-id="24016-115">communication with Azure.</span></span>

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

### <span data-ttu-id="24016-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24016-116">-PassThru</span></span>
<span data-ttu-id="24016-117">Gibt an, dass dieses Cmdlet einen **booleschen** Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="24016-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="24016-118">Dieses Cmdlet gibt standardmäßig keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="24016-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="24016-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="24016-119">-Policy</span></span>
<span data-ttu-id="24016-120">Gibt den Namen der gespeicherten Zugriffsrichtlinie an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="24016-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24016-121">-Table</span><span class="sxs-lookup"><span data-stu-id="24016-121">-Table</span></span>
<span data-ttu-id="24016-122">Gibt den Namen der Azure-Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="24016-122">Specifies the Azure table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24016-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24016-123">-Confirm</span></span>
<span data-ttu-id="24016-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="24016-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24016-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="24016-125">-WhatIf</span></span>
<span data-ttu-id="24016-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="24016-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24016-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="24016-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24016-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24016-128">CommonParameters</span></span>
<span data-ttu-id="24016-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24016-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24016-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24016-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24016-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="24016-131">INPUTS</span></span>

### <span data-ttu-id="24016-132">System.String</span><span class="sxs-lookup"><span data-stu-id="24016-132">System.String</span></span>

### <span data-ttu-id="24016-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="24016-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="24016-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="24016-134">OUTPUTS</span></span>

### <span data-ttu-id="24016-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="24016-135">System.Boolean</span></span>

## <span data-ttu-id="24016-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="24016-136">NOTES</span></span>

## <span data-ttu-id="24016-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="24016-137">RELATED LINKS</span></span>

[<span data-ttu-id="24016-138">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="24016-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="24016-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="24016-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="24016-140">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="24016-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="24016-141">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="24016-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)
