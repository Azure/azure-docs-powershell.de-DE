---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 686f7dbe4bba17017e1920dd2c67a05c2ccd5eae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996893"
---
# <span data-ttu-id="b9618-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="b9618-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="b9618-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b9618-102">SYNOPSIS</span></span>
<span data-ttu-id="b9618-103">Entfernt einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="b9618-103">Removes a snapshot.</span></span>

## <span data-ttu-id="b9618-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9618-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9618-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9618-105">DESCRIPTION</span></span>
<span data-ttu-id="b9618-106">Das Cmdlet **Remove-AzSnapshot** entfernt einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="b9618-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="b9618-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9618-107">EXAMPLES</span></span>

### <span data-ttu-id="b9618-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b9618-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="b9618-109">Dieser Befehl entfernt den Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b9618-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b9618-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9618-110">PARAMETERS</span></span>

### <span data-ttu-id="b9618-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9618-111">-AsJob</span></span>
<span data-ttu-id="b9618-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="b9618-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b9618-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9618-113">-DefaultProfile</span></span>
<span data-ttu-id="b9618-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b9618-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9618-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b9618-115">-Force</span></span>
<span data-ttu-id="b9618-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="b9618-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b9618-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9618-117">-ResourceGroupName</span></span>
<span data-ttu-id="b9618-118">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b9618-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9618-119">-Snapshotname</span><span class="sxs-lookup"><span data-stu-id="b9618-119">-SnapshotName</span></span>
<span data-ttu-id="b9618-120">Gibt den Namen eines Schnappschusses an.</span><span class="sxs-lookup"><span data-stu-id="b9618-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9618-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b9618-121">-Confirm</span></span>
<span data-ttu-id="b9618-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9618-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9618-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9618-123">-WhatIf</span></span>
<span data-ttu-id="b9618-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9618-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9618-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9618-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9618-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9618-126">CommonParameters</span></span>
<span data-ttu-id="b9618-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9618-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9618-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9618-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9618-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b9618-129">INPUTS</span></span>

### <span data-ttu-id="b9618-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b9618-130">System.String</span></span>

## <span data-ttu-id="b9618-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b9618-131">OUTPUTS</span></span>

### <span data-ttu-id="b9618-132">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b9618-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b9618-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="b9618-133">NOTES</span></span>

## <span data-ttu-id="b9618-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b9618-134">RELATED LINKS</span></span>
