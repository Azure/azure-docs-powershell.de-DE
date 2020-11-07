---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 6d32ddf53f675f2ab2897e4bb9ec85655e0fcd14
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850487"
---
# <span data-ttu-id="88d1e-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="88d1e-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="88d1e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="88d1e-102">SYNOPSIS</span></span>
<span data-ttu-id="88d1e-103">Entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="88d1e-103">Removes a stored access policy from an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88d1e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="88d1e-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88d1e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88d1e-105">DESCRIPTION</span></span>
<span data-ttu-id="88d1e-106">Das Cmdlet " **Remove-AzureStorageTableStoredAccessPolicy** " entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="88d1e-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="88d1e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88d1e-107">EXAMPLES</span></span>

### <span data-ttu-id="88d1e-108">Beispiel 1: Entfernen einer gespeicherten Zugriffsrichtlinie aus einer Speichertabelle</span><span class="sxs-lookup"><span data-stu-id="88d1e-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="88d1e-109">Dieser Befehl entfernt die Richtlinie mit dem Namen Policy05 aus der Speichertabelle mit dem Namen myTable.</span><span class="sxs-lookup"><span data-stu-id="88d1e-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="88d1e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="88d1e-110">PARAMETERS</span></span>

### <span data-ttu-id="88d1e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="88d1e-111">-Context</span></span>
<span data-ttu-id="88d1e-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="88d1e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="88d1e-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="88d1e-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="88d1e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88d1e-114">-DefaultProfile</span></span>
<span data-ttu-id="88d1e-115">Kommunikation mit Azure.</span><span class="sxs-lookup"><span data-stu-id="88d1e-115">communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88d1e-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88d1e-116">-PassThru</span></span>
<span data-ttu-id="88d1e-117">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="88d1e-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="88d1e-118">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="88d1e-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="88d1e-119">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="88d1e-119">-Policy</span></span>
<span data-ttu-id="88d1e-120">Gibt den Namen der gespeicherten Zugriffsrichtlinie an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="88d1e-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="88d1e-121">-Tabelle</span><span class="sxs-lookup"><span data-stu-id="88d1e-121">-Table</span></span>
<span data-ttu-id="88d1e-122">Gibt den Namen der Azure-Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="88d1e-122">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="88d1e-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="88d1e-123">-Confirm</span></span>
<span data-ttu-id="88d1e-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="88d1e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88d1e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88d1e-125">-WhatIf</span></span>
<span data-ttu-id="88d1e-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88d1e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88d1e-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88d1e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88d1e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88d1e-128">CommonParameters</span></span>
<span data-ttu-id="88d1e-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88d1e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88d1e-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88d1e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88d1e-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="88d1e-131">INPUTS</span></span>

### <span data-ttu-id="88d1e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="88d1e-132">System.String</span></span>

### <span data-ttu-id="88d1e-133">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="88d1e-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="88d1e-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="88d1e-134">OUTPUTS</span></span>

### <span data-ttu-id="88d1e-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="88d1e-135">System.Boolean</span></span>

## <span data-ttu-id="88d1e-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="88d1e-136">NOTES</span></span>

## <span data-ttu-id="88d1e-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="88d1e-137">RELATED LINKS</span></span>

[<span data-ttu-id="88d1e-138">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="88d1e-138">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="88d1e-139">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="88d1e-139">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="88d1e-140">Neu – AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="88d1e-140">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="88d1e-141">Satz-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="88d1e-141">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
