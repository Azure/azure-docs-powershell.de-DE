---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 9df25558c752b47e41bf76f7db128bd127ad0c53
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996717"
---
# <span data-ttu-id="12121-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="12121-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="12121-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12121-102">SYNOPSIS</span></span>
<span data-ttu-id="12121-103">Entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="12121-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="12121-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12121-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12121-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12121-105">DESCRIPTION</span></span>
<span data-ttu-id="12121-106">Das Cmdlet " **Remove-AzStorageTableStoredAccessPolicy** " entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="12121-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="12121-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12121-107">EXAMPLES</span></span>

### <span data-ttu-id="12121-108">Beispiel 1: Entfernen einer gespeicherten Zugriffsrichtlinie aus einer Speichertabelle</span><span class="sxs-lookup"><span data-stu-id="12121-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="12121-109">Dieser Befehl entfernt die Richtlinie mit dem Namen Policy05 aus der Speichertabelle mit dem Namen myTable.</span><span class="sxs-lookup"><span data-stu-id="12121-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="12121-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="12121-110">PARAMETERS</span></span>

### <span data-ttu-id="12121-111">-Context</span><span class="sxs-lookup"><span data-stu-id="12121-111">-Context</span></span>
<span data-ttu-id="12121-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="12121-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="12121-113">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="12121-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="12121-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12121-114">-DefaultProfile</span></span>
<span data-ttu-id="12121-115">Kommunikation mit Azure.</span><span class="sxs-lookup"><span data-stu-id="12121-115">communication with Azure.</span></span>

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

### <span data-ttu-id="12121-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12121-116">-PassThru</span></span>
<span data-ttu-id="12121-117">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="12121-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="12121-118">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="12121-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="12121-119">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="12121-119">-Policy</span></span>
<span data-ttu-id="12121-120">Gibt den Namen der gespeicherten Zugriffsrichtlinie an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="12121-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="12121-121">-Tabelle</span><span class="sxs-lookup"><span data-stu-id="12121-121">-Table</span></span>
<span data-ttu-id="12121-122">Gibt den Namen der Azure-Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="12121-122">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="12121-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12121-123">-Confirm</span></span>
<span data-ttu-id="12121-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12121-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12121-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12121-125">-WhatIf</span></span>
<span data-ttu-id="12121-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12121-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12121-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12121-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12121-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12121-128">CommonParameters</span></span>
<span data-ttu-id="12121-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12121-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12121-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12121-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12121-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12121-131">INPUTS</span></span>

### <span data-ttu-id="12121-132">System. String</span><span class="sxs-lookup"><span data-stu-id="12121-132">System.String</span></span>

### <span data-ttu-id="12121-133">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="12121-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="12121-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12121-134">OUTPUTS</span></span>

### <span data-ttu-id="12121-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12121-135">System.Boolean</span></span>

## <span data-ttu-id="12121-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="12121-136">NOTES</span></span>

## <span data-ttu-id="12121-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12121-137">RELATED LINKS</span></span>

[<span data-ttu-id="12121-138">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="12121-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="12121-139">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="12121-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="12121-140">Neu – AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="12121-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="12121-141">Satz-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="12121-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)
