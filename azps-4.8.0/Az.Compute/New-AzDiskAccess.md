---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173324"
---
# <span data-ttu-id="ac08d-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ac08d-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="ac08d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac08d-102">SYNOPSIS</span></span>
<span data-ttu-id="ac08d-103">Erstellt eine Datenträgerzugriffs Ressource</span><span class="sxs-lookup"><span data-stu-id="ac08d-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="ac08d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac08d-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac08d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac08d-105">DESCRIPTION</span></span>
<span data-ttu-id="ac08d-106">Das Cmdlet " **New-AzDiskAccess** " erstellt eine Datenträgerzugriffs Ressource</span><span class="sxs-lookup"><span data-stu-id="ac08d-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="ac08d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac08d-107">EXAMPLES</span></span>

### <span data-ttu-id="ac08d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ac08d-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="ac08d-109">Mit diesem Befehl wird ein Datenträgerzugriff mit bestimmten Eigenschaften erstellt.</span><span class="sxs-lookup"><span data-stu-id="ac08d-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="ac08d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac08d-110">PARAMETERS</span></span>

### <span data-ttu-id="ac08d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac08d-111">-AsJob</span></span>
<span data-ttu-id="ac08d-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ac08d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac08d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac08d-113">-DefaultProfile</span></span>
<span data-ttu-id="ac08d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ac08d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac08d-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="ac08d-115">-Location</span></span>
<span data-ttu-id="ac08d-116">Gibt den Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="ac08d-116">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac08d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ac08d-117">-Name</span></span>
<span data-ttu-id="ac08d-118">Gibt den Namen eines Datenträgerzugriffs an.</span><span class="sxs-lookup"><span data-stu-id="ac08d-118">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac08d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac08d-119">-ResourceGroupName</span></span>
<span data-ttu-id="ac08d-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ac08d-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ac08d-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ac08d-121">-Confirm</span></span>
<span data-ttu-id="ac08d-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac08d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac08d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac08d-123">-WhatIf</span></span>
<span data-ttu-id="ac08d-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac08d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac08d-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac08d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac08d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac08d-126">CommonParameters</span></span>
<span data-ttu-id="ac08d-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac08d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac08d-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac08d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac08d-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac08d-129">INPUTS</span></span>

### <span data-ttu-id="ac08d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ac08d-130">System.String</span></span>

## <span data-ttu-id="ac08d-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac08d-131">OUTPUTS</span></span>

### <span data-ttu-id="ac08d-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ac08d-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="ac08d-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac08d-133">NOTES</span></span>

## <span data-ttu-id="ac08d-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac08d-134">RELATED LINKS</span></span>
