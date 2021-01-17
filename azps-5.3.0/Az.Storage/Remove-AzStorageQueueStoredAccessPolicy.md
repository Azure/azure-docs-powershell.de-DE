---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: f5620baf0cbd2f5c195b981787ac9def98851fe2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460207"
---
# <span data-ttu-id="ae5f5-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ae5f5-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="ae5f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae5f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ae5f5-103">Entfernt eine Richtlinie für den gespeicherten Zugriff aus einer Azure-Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="ae5f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae5f5-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae5f5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae5f5-105">DESCRIPTION</span></span>
<span data-ttu-id="ae5f5-106">Das **Cmdlet "Remove-AzStorageQueueStoredAccessPolicy"** entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure-Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="ae5f5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ae5f5-107">EXAMPLES</span></span>

### <span data-ttu-id="ae5f5-108">Beispiel 1: Entfernen einer gespeicherten Zugriffsrichtlinie aus einer Speicherwarteschlange</span><span class="sxs-lookup"><span data-stu-id="ae5f5-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="ae5f5-109">Mit diesem Befehl wird eine Zugriffsrichtlinie mit dem Namen "Policy04" aus der Speicherwarteschlange namens "MyQueue" entfernt.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="ae5f5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae5f5-110">PARAMETERS</span></span>

### <span data-ttu-id="ae5f5-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ae5f5-111">-Context</span></span>
<span data-ttu-id="ae5f5-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ae5f5-113">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ae5f5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae5f5-114">-DefaultProfile</span></span>
<span data-ttu-id="ae5f5-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae5f5-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae5f5-116">-PassThru</span></span>
<span data-ttu-id="ae5f5-117">Gibt an, dass dieses Cmdlet einen **booleschen** Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ae5f5-118">Dieses Cmdlet gibt standardmäßig keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ae5f5-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="ae5f5-119">-Policy</span></span>
<span data-ttu-id="ae5f5-120">Gibt den Namen der gespeicherten Zugriffsrichtlinie an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ae5f5-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="ae5f5-121">-Queue</span></span>
<span data-ttu-id="ae5f5-122">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-122">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="ae5f5-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae5f5-123">-Confirm</span></span>
<span data-ttu-id="ae5f5-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae5f5-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ae5f5-125">-WhatIf</span></span>
<span data-ttu-id="ae5f5-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae5f5-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae5f5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae5f5-128">CommonParameters</span></span>
<span data-ttu-id="ae5f5-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae5f5-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae5f5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae5f5-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ae5f5-131">INPUTS</span></span>

### <span data-ttu-id="ae5f5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ae5f5-132">System.String</span></span>

### <span data-ttu-id="ae5f5-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ae5f5-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ae5f5-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ae5f5-134">OUTPUTS</span></span>

### <span data-ttu-id="ae5f5-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ae5f5-135">System.Boolean</span></span>

## <span data-ttu-id="ae5f5-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ae5f5-136">NOTES</span></span>

## <span data-ttu-id="ae5f5-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ae5f5-137">RELATED LINKS</span></span>

[<span data-ttu-id="ae5f5-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ae5f5-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ae5f5-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ae5f5-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="ae5f5-140">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ae5f5-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ae5f5-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ae5f5-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
