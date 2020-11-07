---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeue
schema: 2.0.0
ms.openlocfilehash: e2fcfa1d100f460bcf352cc26fd0e094d52cad21
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849411"
---
# <span data-ttu-id="32b96-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="32b96-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="32b96-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="32b96-102">SYNOPSIS</span></span>
<span data-ttu-id="32b96-103">Entfernt eine Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="32b96-103">Removes a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32b96-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="32b96-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32b96-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32b96-105">DESCRIPTION</span></span>
<span data-ttu-id="32b96-106">Das Cmdlet **Remove-AzureStorageQueue** entfernt eine Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="32b96-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="32b96-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="32b96-107">EXAMPLES</span></span>

### <span data-ttu-id="32b96-108">Beispiel 1: Entfernen einer Speicherwarteschlange nach Namen</span><span class="sxs-lookup"><span data-stu-id="32b96-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="32b96-109">Dieser Befehl entfernt eine Warteschlange mit dem Namen ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="32b96-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="32b96-110">Beispiel 2: Entfernen mehrerer Speicher Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="32b96-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="32b96-111">Mit diesem Befehl werden alle Warteschlangen mit Namen entfernt, die mit Contoso beginnen.</span><span class="sxs-lookup"><span data-stu-id="32b96-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="32b96-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="32b96-112">PARAMETERS</span></span>

### <span data-ttu-id="32b96-113">-Context</span><span class="sxs-lookup"><span data-stu-id="32b96-113">-Context</span></span>
<span data-ttu-id="32b96-114">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="32b96-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="32b96-115">Zum Abrufen des Speicher Kontexts das New-AzureStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32b96-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="32b96-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b96-116">-DefaultProfile</span></span>
<span data-ttu-id="32b96-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="32b96-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32b96-118">-Force</span><span class="sxs-lookup"><span data-stu-id="32b96-118">-Force</span></span>
<span data-ttu-id="32b96-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="32b96-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="32b96-120">-Name</span><span class="sxs-lookup"><span data-stu-id="32b96-120">-Name</span></span>
<span data-ttu-id="32b96-121">Gibt den Namen der zu entfernenden Warteschlange an.</span><span class="sxs-lookup"><span data-stu-id="32b96-121">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="32b96-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32b96-122">-PassThru</span></span>
<span data-ttu-id="32b96-123">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="32b96-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="32b96-124">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="32b96-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="32b96-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="32b96-125">-Confirm</span></span>
<span data-ttu-id="32b96-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="32b96-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32b96-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32b96-127">-WhatIf</span></span>
<span data-ttu-id="32b96-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32b96-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32b96-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="32b96-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32b96-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b96-130">CommonParameters</span></span>
<span data-ttu-id="32b96-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32b96-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b96-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32b96-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b96-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="32b96-133">INPUTS</span></span>

### <span data-ttu-id="32b96-134">System. String</span><span class="sxs-lookup"><span data-stu-id="32b96-134">System.String</span></span>

### <span data-ttu-id="32b96-135">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="32b96-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="32b96-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="32b96-136">OUTPUTS</span></span>

### <span data-ttu-id="32b96-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="32b96-137">System.Boolean</span></span>

## <span data-ttu-id="32b96-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="32b96-138">NOTES</span></span>

## <span data-ttu-id="32b96-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="32b96-139">RELATED LINKS</span></span>

[<span data-ttu-id="32b96-140">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="32b96-140">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="32b96-141">Neu – AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="32b96-141">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
