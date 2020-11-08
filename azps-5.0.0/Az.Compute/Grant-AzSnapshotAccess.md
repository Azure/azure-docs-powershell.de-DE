---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: a431428c670dba7e0bfb152bde0cae22f47d8099
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177013"
---
# <span data-ttu-id="53d91-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="53d91-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="53d91-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53d91-102">SYNOPSIS</span></span>
<span data-ttu-id="53d91-103">Gewährt einen Zugriff auf einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="53d91-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="53d91-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53d91-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53d91-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53d91-105">DESCRIPTION</span></span>
<span data-ttu-id="53d91-106">Das Cmdlet **Grant-AzSnapshotAccess** gewährt einen Zugriff auf einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="53d91-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="53d91-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53d91-107">EXAMPLES</span></span>

### <span data-ttu-id="53d91-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="53d91-108">Example 1</span></span>
```
PS C:\> Grant-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="53d91-109">Gewähren Sie "Read"-Zugriff auf den Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" für 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="53d91-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="53d91-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="53d91-110">PARAMETERS</span></span>

### <span data-ttu-id="53d91-111">-Access</span><span class="sxs-lookup"><span data-stu-id="53d91-111">-Access</span></span>
<span data-ttu-id="53d91-112">Gibt die Zugriffsebene an.</span><span class="sxs-lookup"><span data-stu-id="53d91-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="53d91-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53d91-113">-AsJob</span></span>
<span data-ttu-id="53d91-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="53d91-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53d91-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53d91-115">-DefaultProfile</span></span>
<span data-ttu-id="53d91-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="53d91-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53d91-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="53d91-117">-DurationInSecond</span></span>
<span data-ttu-id="53d91-118">Gibt die Zugriffsdauer in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="53d91-118">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="53d91-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53d91-119">-ResourceGroupName</span></span>
<span data-ttu-id="53d91-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="53d91-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="53d91-121">-Snapshotname</span><span class="sxs-lookup"><span data-stu-id="53d91-121">-SnapshotName</span></span>
<span data-ttu-id="53d91-122">Gibt den Namen eines Schnappschusses an.</span><span class="sxs-lookup"><span data-stu-id="53d91-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="53d91-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="53d91-123">-Confirm</span></span>
<span data-ttu-id="53d91-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="53d91-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53d91-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53d91-125">-WhatIf</span></span>
<span data-ttu-id="53d91-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="53d91-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53d91-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="53d91-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53d91-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53d91-128">CommonParameters</span></span>
<span data-ttu-id="53d91-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53d91-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53d91-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53d91-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53d91-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53d91-131">INPUTS</span></span>

### <span data-ttu-id="53d91-132">System. String</span><span class="sxs-lookup"><span data-stu-id="53d91-132">System.String</span></span>

## <span data-ttu-id="53d91-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53d91-133">OUTPUTS</span></span>

### <span data-ttu-id="53d91-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="53d91-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="53d91-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="53d91-135">NOTES</span></span>

## <span data-ttu-id="53d91-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53d91-136">RELATED LINKS</span></span>
