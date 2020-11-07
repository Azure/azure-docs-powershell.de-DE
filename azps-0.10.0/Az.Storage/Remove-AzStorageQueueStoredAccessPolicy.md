---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 74189f488519c903e8e02b1e86585d03a9e80446
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842915"
---
# <span data-ttu-id="4c8bb-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4c8bb-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="4c8bb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4c8bb-102">SYNOPSIS</span></span>
<span data-ttu-id="4c8bb-103">Entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure Storage-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="4c8bb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c8bb-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c8bb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c8bb-105">DESCRIPTION</span></span>
<span data-ttu-id="4c8bb-106">Das Cmdlet " **Remove-AzStorageQueueStoredAccessPolicy** " entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure Storage-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="4c8bb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c8bb-107">EXAMPLES</span></span>

### <span data-ttu-id="4c8bb-108">Beispiel 1: Entfernen einer gespeicherten Zugriffsrichtlinie aus einer Speicherwarteschlange</span><span class="sxs-lookup"><span data-stu-id="4c8bb-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="4c8bb-109">Dieser Befehl entfernt eine Access-Richtlinie mit dem Namen Policy04 aus der Speicherwarteschlange mit dem Namen myQueue.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="4c8bb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c8bb-110">PARAMETERS</span></span>

### <span data-ttu-id="4c8bb-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4c8bb-111">-Context</span></span>
<span data-ttu-id="4c8bb-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4c8bb-113">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4c8bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c8bb-114">-DefaultProfile</span></span>
<span data-ttu-id="4c8bb-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c8bb-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c8bb-116">-PassThru</span></span>
<span data-ttu-id="4c8bb-117">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="4c8bb-118">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4c8bb-119">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="4c8bb-119">-Policy</span></span>
<span data-ttu-id="4c8bb-120">Gibt den Namen der gespeicherten Zugriffsrichtlinie an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4c8bb-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="4c8bb-121">-Queue</span></span>
<span data-ttu-id="4c8bb-122">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-122">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="4c8bb-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4c8bb-123">-Confirm</span></span>
<span data-ttu-id="4c8bb-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c8bb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c8bb-125">-WhatIf</span></span>
<span data-ttu-id="4c8bb-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c8bb-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c8bb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c8bb-128">CommonParameters</span></span>
<span data-ttu-id="4c8bb-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c8bb-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c8bb-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c8bb-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4c8bb-131">INPUTS</span></span>

### <span data-ttu-id="4c8bb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4c8bb-132">System.String</span></span>

### <span data-ttu-id="4c8bb-133">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4c8bb-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4c8bb-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4c8bb-134">OUTPUTS</span></span>

### <span data-ttu-id="4c8bb-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4c8bb-135">System.Boolean</span></span>

## <span data-ttu-id="4c8bb-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="4c8bb-136">NOTES</span></span>

## <span data-ttu-id="4c8bb-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4c8bb-137">RELATED LINKS</span></span>

[<span data-ttu-id="4c8bb-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4c8bb-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="4c8bb-139">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4c8bb-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="4c8bb-140">Neu – AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4c8bb-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="4c8bb-141">Satz-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4c8bb-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
