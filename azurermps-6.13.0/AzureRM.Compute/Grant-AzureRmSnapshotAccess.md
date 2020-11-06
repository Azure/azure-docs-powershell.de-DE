---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
ms.openlocfilehash: b60abc403beea938e24ffaa59e634a36611d150b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496338"
---
# <span data-ttu-id="7c906-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="7c906-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="7c906-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c906-102">SYNOPSIS</span></span>
<span data-ttu-id="7c906-103">Gewährt einen Zugriff auf einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="7c906-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c906-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c906-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7c906-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c906-105">DESCRIPTION</span></span>
<span data-ttu-id="7c906-106">Das Cmdlet **Grant-AzureRmSnapshotAccess** gewährt einen Zugriff auf einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="7c906-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="7c906-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c906-107">EXAMPLES</span></span>

### <span data-ttu-id="7c906-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7c906-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="7c906-109">Gewähren Sie "Read"-Zugriff auf den Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" für 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="7c906-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="7c906-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c906-110">PARAMETERS</span></span>

### <span data-ttu-id="7c906-111">-Access</span><span class="sxs-lookup"><span data-stu-id="7c906-111">-Access</span></span>
<span data-ttu-id="7c906-112">Gibt die Zugriffsebene an.</span><span class="sxs-lookup"><span data-stu-id="7c906-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c906-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c906-113">-AsJob</span></span>
<span data-ttu-id="7c906-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7c906-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c906-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c906-115">-DefaultProfile</span></span>
<span data-ttu-id="7c906-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7c906-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c906-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="7c906-117">-DurationInSecond</span></span>
<span data-ttu-id="7c906-118">Gibt die Zugriffsdauer in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="7c906-118">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c906-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c906-119">-ResourceGroupName</span></span>
<span data-ttu-id="7c906-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7c906-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c906-121">-Snapshotname</span><span class="sxs-lookup"><span data-stu-id="7c906-121">-SnapshotName</span></span>
<span data-ttu-id="7c906-122">Gibt den Namen eines Schnappschusses an.</span><span class="sxs-lookup"><span data-stu-id="7c906-122">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c906-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7c906-123">-Confirm</span></span>
<span data-ttu-id="7c906-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c906-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c906-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c906-125">-WhatIf</span></span>
<span data-ttu-id="7c906-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c906-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c906-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c906-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c906-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c906-128">CommonParameters</span></span>
<span data-ttu-id="7c906-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c906-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c906-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c906-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c906-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c906-131">INPUTS</span></span>

### <span data-ttu-id="7c906-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7c906-132">System.String</span></span>

## <span data-ttu-id="7c906-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c906-133">OUTPUTS</span></span>

### <span data-ttu-id="7c906-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="7c906-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="7c906-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c906-135">NOTES</span></span>

## <span data-ttu-id="7c906-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c906-136">RELATED LINKS</span></span>
