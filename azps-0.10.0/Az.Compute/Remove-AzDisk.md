---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: 9e3a194d1143134b1ba3aa472db61062baf847f1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844419"
---
# <span data-ttu-id="579f4-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="579f4-101">Remove-AzDisk</span></span>

## <span data-ttu-id="579f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="579f4-102">SYNOPSIS</span></span>
<span data-ttu-id="579f4-103">Entfernt einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="579f4-103">Removes a disk.</span></span>

## <span data-ttu-id="579f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="579f4-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="579f4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="579f4-105">DESCRIPTION</span></span>
<span data-ttu-id="579f4-106">Das Cmdlet **Remove-AzDisk** entfernt einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="579f4-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="579f4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="579f4-107">EXAMPLES</span></span>

### <span data-ttu-id="579f4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="579f4-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="579f4-109">Dieser Befehl entfernt den Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="579f4-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="579f4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="579f4-110">PARAMETERS</span></span>

### <span data-ttu-id="579f4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="579f4-111">-AsJob</span></span>
<span data-ttu-id="579f4-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="579f4-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="579f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="579f4-113">-DefaultProfile</span></span>
<span data-ttu-id="579f4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="579f4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="579f4-115">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="579f4-115">-DiskName</span></span>
<span data-ttu-id="579f4-116">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="579f4-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="579f4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="579f4-117">-Force</span></span>
<span data-ttu-id="579f4-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="579f4-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="579f4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="579f4-119">-ResourceGroupName</span></span>
<span data-ttu-id="579f4-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="579f4-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="579f4-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="579f4-121">-Confirm</span></span>
<span data-ttu-id="579f4-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="579f4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="579f4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="579f4-123">-WhatIf</span></span>
<span data-ttu-id="579f4-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="579f4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="579f4-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="579f4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="579f4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="579f4-126">CommonParameters</span></span>
<span data-ttu-id="579f4-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="579f4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="579f4-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="579f4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="579f4-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="579f4-129">INPUTS</span></span>

### <span data-ttu-id="579f4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="579f4-130">System.String</span></span>

## <span data-ttu-id="579f4-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="579f4-131">OUTPUTS</span></span>

### <span data-ttu-id="579f4-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="579f4-132">System.Object</span></span>

## <span data-ttu-id="579f4-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="579f4-133">NOTES</span></span>

## <span data-ttu-id="579f4-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="579f4-134">RELATED LINKS</span></span>

