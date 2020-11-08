---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: 39565aa0675a0afc5f6f3996cad522b435a1a9b2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165885"
---
# <span data-ttu-id="a1b5a-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a1b5a-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="a1b5a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a1b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b5a-103">Gewährt einen Zugriff auf einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="a1b5a-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="a1b5a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1b5a-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1b5a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1b5a-105">DESCRIPTION</span></span>
<span data-ttu-id="a1b5a-106">Das Cmdlet **Grant-AzDiskAccess** gewährt einen Zugriff auf einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="a1b5a-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="a1b5a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1b5a-107">EXAMPLES</span></span>

### <span data-ttu-id="a1b5a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a1b5a-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="a1b5a-109">Gewähren Sie "Read"-Zugriff auf den Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" für 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="a1b5a-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="a1b5a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1b5a-110">PARAMETERS</span></span>

### <span data-ttu-id="a1b5a-111">-Access</span><span class="sxs-lookup"><span data-stu-id="a1b5a-111">-Access</span></span>
<span data-ttu-id="a1b5a-112">Gibt die Zugriffsebene an.</span><span class="sxs-lookup"><span data-stu-id="a1b5a-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b5a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1b5a-113">-AsJob</span></span>
<span data-ttu-id="a1b5a-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a1b5a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1b5a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b5a-115">-DefaultProfile</span></span>
<span data-ttu-id="a1b5a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a1b5a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1b5a-117">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="a1b5a-117">-DiskName</span></span>
<span data-ttu-id="a1b5a-118">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="a1b5a-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="a1b5a-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="a1b5a-119">-DurationInSecond</span></span>
<span data-ttu-id="a1b5a-120">Gibt die Zugriffsdauer in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="a1b5a-120">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b5a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1b5a-121">-ResourceGroupName</span></span>
<span data-ttu-id="a1b5a-122">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a1b5a-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a1b5a-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a1b5a-123">-Confirm</span></span>
<span data-ttu-id="a1b5a-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a1b5a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1b5a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1b5a-125">-WhatIf</span></span>
<span data-ttu-id="a1b5a-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1b5a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1b5a-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1b5a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1b5a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b5a-128">CommonParameters</span></span>
<span data-ttu-id="a1b5a-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1b5a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b5a-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1b5a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b5a-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a1b5a-131">INPUTS</span></span>

### <span data-ttu-id="a1b5a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a1b5a-132">System.String</span></span>

## <span data-ttu-id="a1b5a-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a1b5a-133">OUTPUTS</span></span>

### <span data-ttu-id="a1b5a-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="a1b5a-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="a1b5a-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="a1b5a-135">NOTES</span></span>

## <span data-ttu-id="a1b5a-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a1b5a-136">RELATED LINKS</span></span>
