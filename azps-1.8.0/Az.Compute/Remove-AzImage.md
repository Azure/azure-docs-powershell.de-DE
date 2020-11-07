---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: 5d496d4d79c13208c3c48a9d01bfe010ef64c244
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661492"
---
# <span data-ttu-id="7ebf6-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="7ebf6-101">Remove-AzImage</span></span>

## <span data-ttu-id="7ebf6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ebf6-102">SYNOPSIS</span></span>
<span data-ttu-id="7ebf6-103">Entfernt ein Bild.</span><span class="sxs-lookup"><span data-stu-id="7ebf6-103">Removes an image.</span></span>

## <span data-ttu-id="7ebf6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ebf6-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ebf6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ebf6-105">DESCRIPTION</span></span>
<span data-ttu-id="7ebf6-106">Mit dem Cmdlet **Remove-AzImage** wird ein Bild entfernt.</span><span class="sxs-lookup"><span data-stu-id="7ebf6-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="7ebf6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ebf6-107">EXAMPLES</span></span>

### <span data-ttu-id="7ebf6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7ebf6-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="7ebf6-109">Dieser Befehl entfernt das Bild mit dem Namen "Image01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="7ebf6-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="7ebf6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ebf6-110">PARAMETERS</span></span>

### <span data-ttu-id="7ebf6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ebf6-111">-AsJob</span></span>
<span data-ttu-id="7ebf6-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="7ebf6-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7ebf6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ebf6-113">-DefaultProfile</span></span>
<span data-ttu-id="7ebf6-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7ebf6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ebf6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7ebf6-115">-Force</span></span>
<span data-ttu-id="7ebf6-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="7ebf6-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7ebf6-117">-Bildname</span><span class="sxs-lookup"><span data-stu-id="7ebf6-117">-ImageName</span></span>
<span data-ttu-id="7ebf6-118">Gibt den Namen eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="7ebf6-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="7ebf6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ebf6-119">-ResourceGroupName</span></span>
<span data-ttu-id="7ebf6-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7ebf6-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7ebf6-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7ebf6-121">-Confirm</span></span>
<span data-ttu-id="7ebf6-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7ebf6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ebf6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ebf6-123">-WhatIf</span></span>
<span data-ttu-id="7ebf6-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ebf6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ebf6-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7ebf6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ebf6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ebf6-126">CommonParameters</span></span>
<span data-ttu-id="7ebf6-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ebf6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ebf6-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ebf6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ebf6-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ebf6-129">INPUTS</span></span>

### <span data-ttu-id="7ebf6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7ebf6-130">System.String</span></span>

## <span data-ttu-id="7ebf6-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ebf6-131">OUTPUTS</span></span>

### <span data-ttu-id="7ebf6-132">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="7ebf6-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="7ebf6-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ebf6-133">NOTES</span></span>

## <span data-ttu-id="7ebf6-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ebf6-134">RELATED LINKS</span></span>
