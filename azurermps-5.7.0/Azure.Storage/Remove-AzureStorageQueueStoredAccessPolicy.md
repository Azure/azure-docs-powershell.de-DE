---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 5bfdca4637f4d1504d8dbf18a923f8c1f0c082bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665227"
---
# <span data-ttu-id="8de6e-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8de6e-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="8de6e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8de6e-102">SYNOPSIS</span></span>
<span data-ttu-id="8de6e-103">Entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure Storage-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="8de6e-103">Removes a stored access policy from an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8de6e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8de6e-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8de6e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8de6e-105">DESCRIPTION</span></span>
<span data-ttu-id="8de6e-106">Das Cmdlet " **Remove-AzureStorageQueueStoredAccessPolicy** " entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure Storage-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="8de6e-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="8de6e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8de6e-107">EXAMPLES</span></span>

### <span data-ttu-id="8de6e-108">Beispiel 1: Entfernen einer gespeicherten Zugriffsrichtlinie aus einer Speicherwarteschlange</span><span class="sxs-lookup"><span data-stu-id="8de6e-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="8de6e-109">Dieser Befehl entfernt eine Access-Richtlinie mit dem Namen Policy04 aus der Speicherwarteschlange mit dem Namen myQueue.</span><span class="sxs-lookup"><span data-stu-id="8de6e-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="8de6e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8de6e-110">PARAMETERS</span></span>

### <span data-ttu-id="8de6e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="8de6e-111">-Context</span></span>
<span data-ttu-id="8de6e-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="8de6e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8de6e-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8de6e-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8de6e-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8de6e-114">-PassThru</span></span>
<span data-ttu-id="8de6e-115">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="8de6e-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="8de6e-116">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8de6e-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="8de6e-117">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="8de6e-117">-Policy</span></span>
<span data-ttu-id="8de6e-118">Gibt den Namen der gespeicherten Zugriffsrichtlinie an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8de6e-118">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8de6e-119">-Queue</span><span class="sxs-lookup"><span data-stu-id="8de6e-119">-Queue</span></span>
<span data-ttu-id="8de6e-120">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="8de6e-120">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="8de6e-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8de6e-121">-Confirm</span></span>
<span data-ttu-id="8de6e-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8de6e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8de6e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8de6e-123">-WhatIf</span></span>
<span data-ttu-id="8de6e-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8de6e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8de6e-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8de6e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8de6e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de6e-126">CommonParameters</span></span>
<span data-ttu-id="8de6e-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8de6e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de6e-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8de6e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de6e-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8de6e-129">INPUTS</span></span>

### <span data-ttu-id="8de6e-130">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8de6e-130">IStorageContext</span></span>

<span data-ttu-id="8de6e-131">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8de6e-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="8de6e-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8de6e-132">OUTPUTS</span></span>

### <span data-ttu-id="8de6e-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8de6e-133">System.Boolean</span></span>

## <span data-ttu-id="8de6e-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="8de6e-134">NOTES</span></span>

## <span data-ttu-id="8de6e-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8de6e-135">RELATED LINKS</span></span>

[<span data-ttu-id="8de6e-136">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8de6e-136">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="8de6e-137">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="8de6e-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="8de6e-138">Neu – AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8de6e-138">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="8de6e-139">Satz-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8de6e-139">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
