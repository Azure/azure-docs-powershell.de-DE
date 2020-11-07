---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 9c37421ff33bfb7f2a2308512e28fa8373ee308c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848367"
---
# <span data-ttu-id="dd690-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dd690-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="dd690-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd690-102">SYNOPSIS</span></span>
<span data-ttu-id="dd690-103">Entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure Storage-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="dd690-103">Removes a stored access policy from an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd690-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd690-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd690-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd690-105">DESCRIPTION</span></span>
<span data-ttu-id="dd690-106">Das Cmdlet " **Remove-AzureStorageQueueStoredAccessPolicy** " entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure Storage-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="dd690-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="dd690-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd690-107">EXAMPLES</span></span>

### <span data-ttu-id="dd690-108">Beispiel 1: Entfernen einer gespeicherten Zugriffsrichtlinie aus einer Speicherwarteschlange</span><span class="sxs-lookup"><span data-stu-id="dd690-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="dd690-109">Dieser Befehl entfernt eine Access-Richtlinie mit dem Namen Policy04 aus der Speicherwarteschlange mit dem Namen myQueue.</span><span class="sxs-lookup"><span data-stu-id="dd690-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="dd690-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd690-110">PARAMETERS</span></span>

### <span data-ttu-id="dd690-111">-Context</span><span class="sxs-lookup"><span data-stu-id="dd690-111">-Context</span></span>
<span data-ttu-id="dd690-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="dd690-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="dd690-113">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="dd690-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="dd690-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd690-114">-DefaultProfile</span></span>
<span data-ttu-id="dd690-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd690-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd690-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd690-116">-PassThru</span></span>
<span data-ttu-id="dd690-117">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="dd690-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="dd690-118">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="dd690-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="dd690-119">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="dd690-119">-Policy</span></span>
<span data-ttu-id="dd690-120">Gibt den Namen der gespeicherten Zugriffsrichtlinie an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="dd690-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dd690-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="dd690-121">-Queue</span></span>
<span data-ttu-id="dd690-122">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="dd690-122">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="dd690-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd690-123">-Confirm</span></span>
<span data-ttu-id="dd690-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd690-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd690-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd690-125">-WhatIf</span></span>
<span data-ttu-id="dd690-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd690-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd690-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd690-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd690-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd690-128">CommonParameters</span></span>
<span data-ttu-id="dd690-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd690-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd690-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd690-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd690-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd690-131">INPUTS</span></span>

### <span data-ttu-id="dd690-132">System. String</span><span class="sxs-lookup"><span data-stu-id="dd690-132">System.String</span></span>

### <span data-ttu-id="dd690-133">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dd690-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dd690-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd690-134">OUTPUTS</span></span>

### <span data-ttu-id="dd690-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd690-135">System.Boolean</span></span>

## <span data-ttu-id="dd690-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd690-136">NOTES</span></span>

## <span data-ttu-id="dd690-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd690-137">RELATED LINKS</span></span>

[<span data-ttu-id="dd690-138">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dd690-138">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="dd690-139">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="dd690-139">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="dd690-140">Neu – AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dd690-140">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="dd690-141">Satz-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dd690-141">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
