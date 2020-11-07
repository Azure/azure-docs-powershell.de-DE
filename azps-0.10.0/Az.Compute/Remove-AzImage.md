---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: 7dd0978bc408841c0474445dd3bb29d032d9a52c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844420"
---
# <span data-ttu-id="380a7-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="380a7-101">Remove-AzImage</span></span>

## <span data-ttu-id="380a7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="380a7-102">SYNOPSIS</span></span>
<span data-ttu-id="380a7-103">Entfernt ein Bild.</span><span class="sxs-lookup"><span data-stu-id="380a7-103">Removes an image.</span></span>

## <span data-ttu-id="380a7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="380a7-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="380a7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="380a7-105">DESCRIPTION</span></span>
<span data-ttu-id="380a7-106">Mit dem Cmdlet **Remove-AzImage** wird ein Bild entfernt.</span><span class="sxs-lookup"><span data-stu-id="380a7-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="380a7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="380a7-107">EXAMPLES</span></span>

### <span data-ttu-id="380a7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="380a7-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="380a7-109">Dieser Befehl entfernt das Bild mit dem Namen "Image01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="380a7-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="380a7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="380a7-110">PARAMETERS</span></span>

### <span data-ttu-id="380a7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="380a7-111">-AsJob</span></span>
<span data-ttu-id="380a7-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="380a7-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="380a7-113">-DefaultProfile</span></span>
<span data-ttu-id="380a7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="380a7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380a7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="380a7-115">-Force</span></span>
<span data-ttu-id="380a7-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="380a7-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380a7-117">-Bildname</span><span class="sxs-lookup"><span data-stu-id="380a7-117">-ImageName</span></span>
<span data-ttu-id="380a7-118">Gibt den Namen eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="380a7-118">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380a7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="380a7-119">-ResourceGroupName</span></span>
<span data-ttu-id="380a7-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="380a7-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380a7-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="380a7-121">-Confirm</span></span>
<span data-ttu-id="380a7-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="380a7-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380a7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="380a7-123">-WhatIf</span></span>
<span data-ttu-id="380a7-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="380a7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="380a7-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="380a7-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380a7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="380a7-126">CommonParameters</span></span>
<span data-ttu-id="380a7-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="380a7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="380a7-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="380a7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="380a7-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="380a7-129">INPUTS</span></span>

### <span data-ttu-id="380a7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="380a7-130">System.String</span></span>

## <span data-ttu-id="380a7-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="380a7-131">OUTPUTS</span></span>

### <span data-ttu-id="380a7-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="380a7-132">System.Object</span></span>

## <span data-ttu-id="380a7-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="380a7-133">NOTES</span></span>

## <span data-ttu-id="380a7-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="380a7-134">RELATED LINKS</span></span>

