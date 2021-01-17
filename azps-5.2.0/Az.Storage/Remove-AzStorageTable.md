---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
ms.openlocfilehash: 98ffbfe7153ba0592563b21695e1a4d1c227f99a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303400"
---
# <span data-ttu-id="72df5-101">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="72df5-101">Remove-AzStorageTable</span></span>

## <span data-ttu-id="72df5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72df5-102">SYNOPSIS</span></span>
<span data-ttu-id="72df5-103">Entfernt eine Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="72df5-103">Removes a storage table.</span></span>

## <span data-ttu-id="72df5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72df5-104">SYNTAX</span></span>

```
Remove-AzStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72df5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72df5-105">DESCRIPTION</span></span>
<span data-ttu-id="72df5-106">Das **Cmdlet "Remove-AzStorageTable"** entfernt eine oder mehrere Speichertabellen aus einem Speicherkonto in Azure.</span><span class="sxs-lookup"><span data-stu-id="72df5-106">The **Remove-AzStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="72df5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="72df5-107">EXAMPLES</span></span>

### <span data-ttu-id="72df5-108">Beispiel 1: Entfernen einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="72df5-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzStorageTable -Name "TableABC"
```

<span data-ttu-id="72df5-109">Mit diesem Befehl wird eine Tabelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="72df5-109">This command removes a table.</span></span>

### <span data-ttu-id="72df5-110">Beispiel 2: Entfernen mehrerer Tabellen</span><span class="sxs-lookup"><span data-stu-id="72df5-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzStorageTable table* | Remove-AzStorageTable
```

<span data-ttu-id="72df5-111">In diesem Beispiel wird ein Platzhalterzeichen mit dem Parameter *"Name"* verwendet, um alle Tabellen zu erhalten, die der Mustertabelle entsprechen, und dann das Ergebnis in der Pipeline übergeben, um die Tabellen zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="72df5-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="72df5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72df5-112">PARAMETERS</span></span>

### <span data-ttu-id="72df5-113">-Context</span><span class="sxs-lookup"><span data-stu-id="72df5-113">-Context</span></span>
<span data-ttu-id="72df5-114">Gibt den Azure -Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="72df5-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="72df5-115">Sie können sie mithilfe des cmdlets New-AzStorageContext erstellen.</span><span class="sxs-lookup"><span data-stu-id="72df5-115">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="72df5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72df5-116">-DefaultProfile</span></span>
<span data-ttu-id="72df5-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72df5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72df5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="72df5-118">-Force</span></span>
<span data-ttu-id="72df5-119">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="72df5-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="72df5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="72df5-120">-Name</span></span>
<span data-ttu-id="72df5-121">Gibt den Namen der zu entfernenden Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="72df5-121">Specifies the name of the table to remove.</span></span>

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

### <span data-ttu-id="72df5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72df5-122">-PassThru</span></span>
<span data-ttu-id="72df5-123">Gibt an, dass dieses Cmdlet einen **booleschen** Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="72df5-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="72df5-124">Dieses Cmdlet gibt standardmäßig keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="72df5-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="72df5-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72df5-125">-Confirm</span></span>
<span data-ttu-id="72df5-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72df5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72df5-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="72df5-127">-WhatIf</span></span>
<span data-ttu-id="72df5-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72df5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72df5-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72df5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72df5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72df5-130">CommonParameters</span></span>
<span data-ttu-id="72df5-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72df5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72df5-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72df5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72df5-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="72df5-133">INPUTS</span></span>

### <span data-ttu-id="72df5-134">System.String</span><span class="sxs-lookup"><span data-stu-id="72df5-134">System.String</span></span>

### <span data-ttu-id="72df5-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="72df5-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="72df5-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="72df5-136">OUTPUTS</span></span>

### <span data-ttu-id="72df5-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="72df5-137">System.Boolean</span></span>

## <span data-ttu-id="72df5-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="72df5-138">NOTES</span></span>

## <span data-ttu-id="72df5-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="72df5-139">RELATED LINKS</span></span>

[<span data-ttu-id="72df5-140">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="72df5-140">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)
