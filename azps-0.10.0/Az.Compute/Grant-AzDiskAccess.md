---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: b7c5f713c7c245676804318b880df3f79a7ca60d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844528"
---
# <span data-ttu-id="2ec92-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="2ec92-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="2ec92-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2ec92-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec92-103">Gewährt einen Zugriff auf einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="2ec92-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="2ec92-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ec92-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ec92-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ec92-105">DESCRIPTION</span></span>
<span data-ttu-id="2ec92-106">Das Cmdlet **Grant-AzDiskAccess** gewährt einen Zugriff auf einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="2ec92-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="2ec92-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ec92-107">EXAMPLES</span></span>

### <span data-ttu-id="2ec92-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2ec92-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="2ec92-109">Gewähren Sie "Read"-Zugriff auf den Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" für 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="2ec92-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="2ec92-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ec92-110">PARAMETERS</span></span>

### <span data-ttu-id="2ec92-111">-Access</span><span class="sxs-lookup"><span data-stu-id="2ec92-111">-Access</span></span>
<span data-ttu-id="2ec92-112">Gibt die Zugriffsebene an.</span><span class="sxs-lookup"><span data-stu-id="2ec92-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="2ec92-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ec92-113">-AsJob</span></span>
<span data-ttu-id="2ec92-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2ec92-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ec92-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec92-115">-DefaultProfile</span></span>
<span data-ttu-id="2ec92-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2ec92-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ec92-117">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="2ec92-117">-DiskName</span></span>
<span data-ttu-id="2ec92-118">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="2ec92-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="2ec92-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="2ec92-119">-DurationInSecond</span></span>
<span data-ttu-id="2ec92-120">Gibt die Zugriffsdauer in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="2ec92-120">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="2ec92-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ec92-121">-ResourceGroupName</span></span>
<span data-ttu-id="2ec92-122">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2ec92-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2ec92-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2ec92-123">-Confirm</span></span>
<span data-ttu-id="2ec92-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ec92-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ec92-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ec92-125">-WhatIf</span></span>
<span data-ttu-id="2ec92-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ec92-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ec92-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ec92-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ec92-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec92-128">CommonParameters</span></span>
<span data-ttu-id="2ec92-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ec92-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec92-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ec92-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec92-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2ec92-131">INPUTS</span></span>

### <span data-ttu-id="2ec92-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2ec92-132">System.String</span></span>

## <span data-ttu-id="2ec92-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2ec92-133">OUTPUTS</span></span>

### <span data-ttu-id="2ec92-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="2ec92-134">System.Object</span></span>

## <span data-ttu-id="2ec92-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="2ec92-135">NOTES</span></span>

## <span data-ttu-id="2ec92-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2ec92-136">RELATED LINKS</span></span>

