---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 88b142943e37009cf21b35bdaadfd209d1d74c86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923251"
---
# <span data-ttu-id="5a75a-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5a75a-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="5a75a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a75a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a75a-103">Entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure-Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="5a75a-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="5a75a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a75a-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a75a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a75a-105">DESCRIPTION</span></span>
<span data-ttu-id="5a75a-106">Das **Cmdlet Remove-AzStorageQueueStoredAccessPolicy** entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure-Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="5a75a-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="5a75a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5a75a-107">EXAMPLES</span></span>

### <span data-ttu-id="5a75a-108">Beispiel 1: Entfernen einer gespeicherten Zugriffsrichtlinie aus einer Speicherwarteschlange</span><span class="sxs-lookup"><span data-stu-id="5a75a-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="5a75a-109">Mit diesem Befehl wird eine Zugriffsrichtlinie mit dem Namen "Policy04" aus der Speicherwarteschlange "MyQueue" entfernt.</span><span class="sxs-lookup"><span data-stu-id="5a75a-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="5a75a-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5a75a-110">PARAMETERS</span></span>

### <span data-ttu-id="5a75a-111">-Context</span><span class="sxs-lookup"><span data-stu-id="5a75a-111">-Context</span></span>
<span data-ttu-id="5a75a-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="5a75a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5a75a-113">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a75a-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5a75a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a75a-114">-DefaultProfile</span></span>
<span data-ttu-id="5a75a-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a75a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a75a-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a75a-116">-PassThru</span></span>
<span data-ttu-id="5a75a-117">Gibt an, dass dieses Cmdlet einen **booleschen** Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="5a75a-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="5a75a-118">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5a75a-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="5a75a-119">-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="5a75a-119">-Policy</span></span>
<span data-ttu-id="5a75a-120">Gibt den Namen der gespeicherten Zugriffsrichtlinie an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5a75a-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5a75a-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="5a75a-121">-Queue</span></span>
<span data-ttu-id="5a75a-122">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="5a75a-122">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="5a75a-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5a75a-123">-Confirm</span></span>
<span data-ttu-id="5a75a-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a75a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a75a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a75a-125">-WhatIf</span></span>
<span data-ttu-id="5a75a-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a75a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a75a-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a75a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a75a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a75a-128">CommonParameters</span></span>
<span data-ttu-id="5a75a-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a75a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a75a-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a75a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a75a-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5a75a-131">INPUTS</span></span>

### <span data-ttu-id="5a75a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5a75a-132">System.String</span></span>

### <span data-ttu-id="5a75a-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5a75a-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5a75a-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5a75a-134">OUTPUTS</span></span>

### <span data-ttu-id="5a75a-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5a75a-135">System.Boolean</span></span>

## <span data-ttu-id="5a75a-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5a75a-136">NOTES</span></span>

## <span data-ttu-id="5a75a-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5a75a-137">RELATED LINKS</span></span>

[<span data-ttu-id="5a75a-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5a75a-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="5a75a-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5a75a-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="5a75a-140">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5a75a-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="5a75a-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5a75a-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
