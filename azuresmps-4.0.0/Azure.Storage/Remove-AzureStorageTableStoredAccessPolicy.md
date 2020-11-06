---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3276a23869633238ebc6b84dfa01934e5ad9896
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474877"
---
# <span data-ttu-id="046c0-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="046c0-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="046c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="046c0-102">SYNOPSIS</span></span>
<span data-ttu-id="046c0-103">Entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="046c0-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="046c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="046c0-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="046c0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="046c0-105">DESCRIPTION</span></span>
<span data-ttu-id="046c0-106">Das Cmdlet " **Remove-AzureStorageTableStoredAccessPolicy** " entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="046c0-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="046c0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="046c0-107">EXAMPLES</span></span>

### <span data-ttu-id="046c0-108">Beispiel 1: Entfernen einer gespeicherten Zugriffsrichtlinie aus einer Speichertabelle</span><span class="sxs-lookup"><span data-stu-id="046c0-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="046c0-109">Dieser Befehl entfernt die Richtlinie mit dem Namen Policy05 aus der Speichertabelle mit dem Namen myTable.</span><span class="sxs-lookup"><span data-stu-id="046c0-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="046c0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="046c0-110">PARAMETERS</span></span>

### <span data-ttu-id="046c0-111">-Context</span><span class="sxs-lookup"><span data-stu-id="046c0-111">-Context</span></span>
<span data-ttu-id="046c0-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="046c0-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="046c0-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="046c0-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="046c0-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="046c0-114">-PassThru</span></span>
<span data-ttu-id="046c0-115">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="046c0-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="046c0-116">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="046c0-116">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="046c0-117">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="046c0-117">-Policy</span></span>
<span data-ttu-id="046c0-118">Gibt die Richtlinie für den gespeicherten Zugriff an, die die Berechtigungen für dieses SAS-Token umfasst.</span><span class="sxs-lookup"><span data-stu-id="046c0-118">Specifies the stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046c0-119">-Tabelle</span><span class="sxs-lookup"><span data-stu-id="046c0-119">-Table</span></span>
<span data-ttu-id="046c0-120">Gibt den Namen der Azure-Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="046c0-120">Specifies the Azure table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046c0-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="046c0-121">-Confirm</span></span>
<span data-ttu-id="046c0-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="046c0-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="046c0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="046c0-123">-WhatIf</span></span>
<span data-ttu-id="046c0-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="046c0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="046c0-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="046c0-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="046c0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="046c0-126">CommonParameters</span></span>
<span data-ttu-id="046c0-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="046c0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="046c0-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="046c0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="046c0-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="046c0-129">INPUTS</span></span>

## <span data-ttu-id="046c0-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="046c0-130">OUTPUTS</span></span>

## <span data-ttu-id="046c0-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="046c0-131">NOTES</span></span>

## <span data-ttu-id="046c0-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="046c0-132">RELATED LINKS</span></span>

[<span data-ttu-id="046c0-133">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="046c0-133">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="046c0-134">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="046c0-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="046c0-135">Neu – AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="046c0-135">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="046c0-136">Satz-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="046c0-136">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
