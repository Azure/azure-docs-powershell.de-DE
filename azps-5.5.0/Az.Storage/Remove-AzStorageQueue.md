---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
ms.openlocfilehash: 2cc10a1b72dc369aef08b84e7b8fe2128ff0ac33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165644"
---
# <span data-ttu-id="15c40-101">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="15c40-101">Remove-AzStorageQueue</span></span>

## <span data-ttu-id="15c40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15c40-102">SYNOPSIS</span></span>
<span data-ttu-id="15c40-103">Entfernt eine Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="15c40-103">Removes a storage queue.</span></span>

## <span data-ttu-id="15c40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15c40-104">SYNTAX</span></span>

```
Remove-AzStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15c40-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15c40-105">DESCRIPTION</span></span>
<span data-ttu-id="15c40-106">Das **Cmdlet "Remove-AzStorageQueue"** entfernt eine Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="15c40-106">The **Remove-AzStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="15c40-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="15c40-107">EXAMPLES</span></span>

### <span data-ttu-id="15c40-108">Beispiel 1: Entfernen einer Speicherwarteschlange nach Name</span><span class="sxs-lookup"><span data-stu-id="15c40-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzStorageQueue "ContosoQueue01"
```

<span data-ttu-id="15c40-109">Mit diesem Befehl wird eine Warteschlange namens "ContosoQueue01" entfernt.</span><span class="sxs-lookup"><span data-stu-id="15c40-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="15c40-110">Beispiel 2: Entfernen mehrerer Speicherwarteschlangen</span><span class="sxs-lookup"><span data-stu-id="15c40-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzStorageQueue "Contoso*" | Remove-AzStorageQueue
```

<span data-ttu-id="15c40-111">Mit diesem Befehl werden alle Warteschlangen mit Namen entfernt, die mit Contoso beginnen.</span><span class="sxs-lookup"><span data-stu-id="15c40-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="15c40-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15c40-112">PARAMETERS</span></span>

### <span data-ttu-id="15c40-113">-Context</span><span class="sxs-lookup"><span data-stu-id="15c40-113">-Context</span></span>
<span data-ttu-id="15c40-114">Gibt den Azure -Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="15c40-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="15c40-115">Zum Abrufen des Speicherkontexts wird das New-AzStorageContext cmdlet verwendet.</span><span class="sxs-lookup"><span data-stu-id="15c40-115">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="15c40-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c40-116">-DefaultProfile</span></span>
<span data-ttu-id="15c40-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="15c40-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15c40-118">-Force</span><span class="sxs-lookup"><span data-stu-id="15c40-118">-Force</span></span>
<span data-ttu-id="15c40-119">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="15c40-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="15c40-120">-Name</span><span class="sxs-lookup"><span data-stu-id="15c40-120">-Name</span></span>
<span data-ttu-id="15c40-121">Gibt den Namen der zu entfernenden Warteschlange an.</span><span class="sxs-lookup"><span data-stu-id="15c40-121">Specifies the name of the queue to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15c40-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15c40-122">-PassThru</span></span>
<span data-ttu-id="15c40-123">Gibt an, dass dieses Cmdlet einen **booleschen** Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="15c40-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="15c40-124">Dieses Cmdlet gibt standardmäßig keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="15c40-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="15c40-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15c40-125">-Confirm</span></span>
<span data-ttu-id="15c40-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15c40-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15c40-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="15c40-127">-WhatIf</span></span>
<span data-ttu-id="15c40-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15c40-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15c40-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15c40-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15c40-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c40-130">CommonParameters</span></span>
<span data-ttu-id="15c40-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15c40-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c40-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15c40-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c40-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="15c40-133">INPUTS</span></span>

### <span data-ttu-id="15c40-134">System.String</span><span class="sxs-lookup"><span data-stu-id="15c40-134">System.String</span></span>

### <span data-ttu-id="15c40-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="15c40-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="15c40-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="15c40-136">OUTPUTS</span></span>

### <span data-ttu-id="15c40-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="15c40-137">System.Boolean</span></span>

## <span data-ttu-id="15c40-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="15c40-138">NOTES</span></span>

## <span data-ttu-id="15c40-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="15c40-139">RELATED LINKS</span></span>

[<span data-ttu-id="15c40-140">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="15c40-140">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="15c40-141">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="15c40-141">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)
