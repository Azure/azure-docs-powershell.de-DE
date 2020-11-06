---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: ''
schema: 2.0.0
ms.openlocfilehash: 116dcc8967ab18d0b67cd3e4eeea91190c38930f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475561"
---
# <span data-ttu-id="eb4aa-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eb4aa-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="eb4aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eb4aa-102">SYNOPSIS</span></span>
<span data-ttu-id="eb4aa-103">Entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure Storage-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="eb4aa-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="eb4aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb4aa-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb4aa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb4aa-105">DESCRIPTION</span></span>
<span data-ttu-id="eb4aa-106">Das Cmdlet " **Remove-AzureStorageQueueStoredAccessPolicy** " entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure Storage-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="eb4aa-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="eb4aa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb4aa-107">EXAMPLES</span></span>

### <span data-ttu-id="eb4aa-108">Beispiel 1: Entfernen einer gespeicherten Zugriffsrichtlinie aus einer Speicherwarteschlange</span><span class="sxs-lookup"><span data-stu-id="eb4aa-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="eb4aa-109">Dieser Befehl entfernt eine Access-Richtlinie mit dem Namen Policy04 aus der Speicherwarteschlange mit dem Namen myQueue.</span><span class="sxs-lookup"><span data-stu-id="eb4aa-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="eb4aa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb4aa-110">PARAMETERS</span></span>

### <span data-ttu-id="eb4aa-111">-Context</span><span class="sxs-lookup"><span data-stu-id="eb4aa-111">-Context</span></span>
<span data-ttu-id="eb4aa-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="eb4aa-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="eb4aa-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="eb4aa-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="eb4aa-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb4aa-114">-PassThru</span></span>
<span data-ttu-id="eb4aa-115">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="eb4aa-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="eb4aa-116">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="eb4aa-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="eb4aa-117">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="eb4aa-117">-Policy</span></span>
<span data-ttu-id="eb4aa-118">Gibt die Richtlinie für den gespeicherten Zugriff an, die die Berechtigungen für dieses SAS-Token (Shared Access Signature) enthält.</span><span class="sxs-lookup"><span data-stu-id="eb4aa-118">Specifies the stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="eb4aa-119">-Queue</span><span class="sxs-lookup"><span data-stu-id="eb4aa-119">-Queue</span></span>
<span data-ttu-id="eb4aa-120">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="eb4aa-120">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="eb4aa-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eb4aa-121">-Confirm</span></span>
<span data-ttu-id="eb4aa-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eb4aa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb4aa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb4aa-123">-WhatIf</span></span>
<span data-ttu-id="eb4aa-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb4aa-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb4aa-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb4aa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb4aa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb4aa-126">CommonParameters</span></span>
<span data-ttu-id="eb4aa-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb4aa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb4aa-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb4aa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb4aa-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb4aa-129">INPUTS</span></span>

## <span data-ttu-id="eb4aa-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eb4aa-130">OUTPUTS</span></span>

## <span data-ttu-id="eb4aa-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="eb4aa-131">NOTES</span></span>

## <span data-ttu-id="eb4aa-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eb4aa-132">RELATED LINKS</span></span>

[<span data-ttu-id="eb4aa-133">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eb4aa-133">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="eb4aa-134">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="eb4aa-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="eb4aa-135">Neu – AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eb4aa-135">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="eb4aa-136">Satz-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eb4aa-136">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
