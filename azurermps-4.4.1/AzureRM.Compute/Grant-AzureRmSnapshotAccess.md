---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
ms.openlocfilehash: 9b870214362c6e2bcd7225ef5a40ed5ff780139a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497117"
---
# <span data-ttu-id="66bc4-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="66bc4-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="66bc4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66bc4-102">SYNOPSIS</span></span>
<span data-ttu-id="66bc4-103">Gewährt einen Zugriff auf einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="66bc4-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66bc4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66bc4-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66bc4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66bc4-105">DESCRIPTION</span></span>
<span data-ttu-id="66bc4-106">Das Cmdlet **Grant-AzureRmSnapshotAccess** gewährt einen Zugriff auf einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="66bc4-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="66bc4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66bc4-107">EXAMPLES</span></span>

### <span data-ttu-id="66bc4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="66bc4-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="66bc4-109">Gewähren Sie "Read"-Zugriff auf den Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" für 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="66bc4-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="66bc4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="66bc4-110">PARAMETERS</span></span>

### <span data-ttu-id="66bc4-111">-Access</span><span class="sxs-lookup"><span data-stu-id="66bc4-111">-Access</span></span>
<span data-ttu-id="66bc4-112">Gibt die Zugriffsebene an.</span><span class="sxs-lookup"><span data-stu-id="66bc4-112">Specifies Access level.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66bc4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66bc4-113">-DefaultProfile</span></span>
<span data-ttu-id="66bc4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66bc4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66bc4-115">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="66bc4-115">-DurationInSecond</span></span>
<span data-ttu-id="66bc4-116">Gibt die Zugriffsdauer in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="66bc4-116">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="66bc4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66bc4-117">-ResourceGroupName</span></span>
<span data-ttu-id="66bc4-118">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="66bc4-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="66bc4-119">-Snapshotname</span><span class="sxs-lookup"><span data-stu-id="66bc4-119">-SnapshotName</span></span>
<span data-ttu-id="66bc4-120">Gibt den Namen eines Schnappschusses an.</span><span class="sxs-lookup"><span data-stu-id="66bc4-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="66bc4-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66bc4-121">-Confirm</span></span>
<span data-ttu-id="66bc4-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66bc4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66bc4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66bc4-123">-WhatIf</span></span>
<span data-ttu-id="66bc4-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66bc4-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66bc4-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66bc4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66bc4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66bc4-126">CommonParameters</span></span>
<span data-ttu-id="66bc4-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66bc4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66bc4-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66bc4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66bc4-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66bc4-129">INPUTS</span></span>

### <span data-ttu-id="66bc4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="66bc4-130">System.String</span></span>

## <span data-ttu-id="66bc4-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66bc4-131">OUTPUTS</span></span>

### <span data-ttu-id="66bc4-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="66bc4-132">System.Object</span></span>

## <span data-ttu-id="66bc4-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="66bc4-133">NOTES</span></span>

## <span data-ttu-id="66bc4-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66bc4-134">RELATED LINKS</span></span>

