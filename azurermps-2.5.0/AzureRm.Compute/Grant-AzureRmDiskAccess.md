---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermdiskaccess
schema: 2.0.0
ms.openlocfilehash: c574b273082d3c7e840d589fe765190d99028d89
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849768"
---
# <span data-ttu-id="39e1f-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="39e1f-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="39e1f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39e1f-102">SYNOPSIS</span></span>
<span data-ttu-id="39e1f-103">Gewährt einen Zugriff auf einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="39e1f-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39e1f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39e1f-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39e1f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39e1f-105">DESCRIPTION</span></span>
<span data-ttu-id="39e1f-106">Das Cmdlet **Grant-AzureRmDiskAccess** gewährt einen Zugriff auf einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="39e1f-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="39e1f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39e1f-107">EXAMPLES</span></span>

### <span data-ttu-id="39e1f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="39e1f-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="39e1f-109">Gewähren Sie "Read"-Zugriff auf den Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" für 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="39e1f-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="39e1f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="39e1f-110">PARAMETERS</span></span>

### <span data-ttu-id="39e1f-111">-Access</span><span class="sxs-lookup"><span data-stu-id="39e1f-111">-Access</span></span>
<span data-ttu-id="39e1f-112">Gibt die Zugriffsebene an.</span><span class="sxs-lookup"><span data-stu-id="39e1f-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e1f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39e1f-113">-AsJob</span></span>
<span data-ttu-id="39e1f-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="39e1f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39e1f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39e1f-115">-DefaultProfile</span></span>
<span data-ttu-id="39e1f-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="39e1f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39e1f-117">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="39e1f-117">-DiskName</span></span>
<span data-ttu-id="39e1f-118">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="39e1f-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="39e1f-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="39e1f-119">-DurationInSecond</span></span>
<span data-ttu-id="39e1f-120">Gibt die Zugriffsdauer in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="39e1f-120">Specifies access duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e1f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39e1f-121">-ResourceGroupName</span></span>
<span data-ttu-id="39e1f-122">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="39e1f-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="39e1f-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="39e1f-123">-Confirm</span></span>
<span data-ttu-id="39e1f-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39e1f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39e1f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39e1f-125">-WhatIf</span></span>
<span data-ttu-id="39e1f-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39e1f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39e1f-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39e1f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39e1f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39e1f-128">CommonParameters</span></span>
<span data-ttu-id="39e1f-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39e1f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39e1f-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39e1f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39e1f-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39e1f-131">INPUTS</span></span>

### <span data-ttu-id="39e1f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="39e1f-132">System.String</span></span>

## <span data-ttu-id="39e1f-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39e1f-133">OUTPUTS</span></span>

### <span data-ttu-id="39e1f-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="39e1f-134">System.Object</span></span>

## <span data-ttu-id="39e1f-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="39e1f-135">NOTES</span></span>

## <span data-ttu-id="39e1f-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39e1f-136">RELATED LINKS</span></span>

