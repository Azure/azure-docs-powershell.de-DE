---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
ms.openlocfilehash: 98ffbfe7153ba0592563b21695e1a4d1c227f99a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157972"
---
# <span data-ttu-id="93588-101">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="93588-101">Remove-AzStorageTable</span></span>

## <span data-ttu-id="93588-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93588-102">SYNOPSIS</span></span>
<span data-ttu-id="93588-103">Entfernt eine Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="93588-103">Removes a storage table.</span></span>

## <span data-ttu-id="93588-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93588-104">SYNTAX</span></span>

```
Remove-AzStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93588-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93588-105">DESCRIPTION</span></span>
<span data-ttu-id="93588-106">Das **Cmdlet "Remove-AzStorageTable"** entfernt eine oder mehrere Speichertabellen aus einem Speicherkonto in Azure.</span><span class="sxs-lookup"><span data-stu-id="93588-106">The **Remove-AzStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="93588-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="93588-107">EXAMPLES</span></span>

### <span data-ttu-id="93588-108">Beispiel 1: Entfernen einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="93588-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzStorageTable -Name "TableABC"
```

<span data-ttu-id="93588-109">Mit diesem Befehl wird eine Tabelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="93588-109">This command removes a table.</span></span>

### <span data-ttu-id="93588-110">Beispiel 2: Entfernen mehrerer Tabellen</span><span class="sxs-lookup"><span data-stu-id="93588-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzStorageTable table* | Remove-AzStorageTable
```

<span data-ttu-id="93588-111">In diesem Beispiel wird ein Platzhalterzeichen mit dem Parameter *"Name"* verwendet, um alle Tabellen zu erhalten, die der Mustertabelle entsprechen, und dann das Ergebnis in der Pipeline übergeben, um die Tabellen zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="93588-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="93588-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93588-112">PARAMETERS</span></span>

### <span data-ttu-id="93588-113">-Context</span><span class="sxs-lookup"><span data-stu-id="93588-113">-Context</span></span>
<span data-ttu-id="93588-114">Gibt den Azure -Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="93588-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="93588-115">Sie können sie mithilfe des cmdlets New-AzStorageContext erstellen.</span><span class="sxs-lookup"><span data-stu-id="93588-115">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="93588-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93588-116">-DefaultProfile</span></span>
<span data-ttu-id="93588-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93588-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93588-118">-Force</span><span class="sxs-lookup"><span data-stu-id="93588-118">-Force</span></span>
<span data-ttu-id="93588-119">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="93588-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="93588-120">-Name</span><span class="sxs-lookup"><span data-stu-id="93588-120">-Name</span></span>
<span data-ttu-id="93588-121">Gibt den Namen der zu entfernenden Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="93588-121">Specifies the name of the table to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93588-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93588-122">-PassThru</span></span>
<span data-ttu-id="93588-123">Gibt an, dass dieses Cmdlet einen **booleschen** Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="93588-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="93588-124">Dieses Cmdlet gibt standardmäßig keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="93588-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="93588-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93588-125">-Confirm</span></span>
<span data-ttu-id="93588-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="93588-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93588-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="93588-127">-WhatIf</span></span>
<span data-ttu-id="93588-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="93588-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93588-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="93588-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93588-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93588-130">CommonParameters</span></span>
<span data-ttu-id="93588-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93588-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93588-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93588-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93588-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="93588-133">INPUTS</span></span>

### <span data-ttu-id="93588-134">System.String</span><span class="sxs-lookup"><span data-stu-id="93588-134">System.String</span></span>

### <span data-ttu-id="93588-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="93588-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="93588-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="93588-136">OUTPUTS</span></span>

### <span data-ttu-id="93588-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="93588-137">System.Boolean</span></span>

## <span data-ttu-id="93588-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="93588-138">NOTES</span></span>

## <span data-ttu-id="93588-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="93588-139">RELATED LINKS</span></span>

[<span data-ttu-id="93588-140">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="93588-140">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)
