---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af9c5d2c5ebb547a6e09d2e4f4302ed2da470a39
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007260"
---
# <span data-ttu-id="259d4-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="259d4-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="259d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="259d4-102">SYNOPSIS</span></span>
<span data-ttu-id="259d4-103">Startet einen Container Migrationsauftrag zum Migrieren von Containern zur angegebenen Zielfreigabe.</span><span class="sxs-lookup"><span data-stu-id="259d4-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="259d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="259d4-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-ContainerName] <String>
 [-ShareName] <String> [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="259d4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="259d4-105">DESCRIPTION</span></span>
<span data-ttu-id="259d4-106">Startet einen Container Migrationsauftrag zum Migrieren von Containern zur angegebenen Zielfreigabe.</span><span class="sxs-lookup"><span data-stu-id="259d4-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="259d4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="259d4-107">EXAMPLES</span></span>

### <span data-ttu-id="259d4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="259d4-108">EXAMPLE 1</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -ContainerName "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="259d4-109">Startet eine Container Migration.</span><span class="sxs-lookup"><span data-stu-id="259d4-109">Starts a container migration.</span></span>

## <span data-ttu-id="259d4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="259d4-110">PARAMETERS</span></span>

### <span data-ttu-id="259d4-111">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="259d4-111">-StorageAccountName</span></span>
<span data-ttu-id="259d4-112">Der Name des speicherkontos, in dem der Container gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="259d4-112">The name of storage account where the container locates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259d4-113">-Containername</span><span class="sxs-lookup"><span data-stu-id="259d4-113">-ContainerName</span></span>
<span data-ttu-id="259d4-114">Der Name des zu migrierenden Containers.</span><span class="sxs-lookup"><span data-stu-id="259d4-114">The name of the container to be migrated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259d4-115">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="259d4-115">-ShareName</span></span>
<span data-ttu-id="259d4-116">Der Name der Freigabe, die den für die Migration angegebenen Container enthält.</span><span class="sxs-lookup"><span data-stu-id="259d4-116">Name of the share containing the container specified for migration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259d4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="259d4-117">-ResourceGroupName</span></span>
<span data-ttu-id="259d4-118">Der Name der Ressourcengruppe, unter der der Speicherressourcen Anbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="259d4-118">The resource group name in which the storage resource provider was registered under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259d4-119">-Farmname</span><span class="sxs-lookup"><span data-stu-id="259d4-119">-FarmName</span></span>
<span data-ttu-id="259d4-120">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="259d4-120">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259d4-121">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="259d4-121">-DestinationShareUncPath</span></span>
<span data-ttu-id="259d4-122">Der UNC-Pfad der Zielfreigabe für die Migration.</span><span class="sxs-lookup"><span data-stu-id="259d4-122">The UNC path of the destination share for migration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259d4-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="259d4-123">-AsJob</span></span>
<span data-ttu-id="259d4-124">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="259d4-124">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259d4-125">-Force</span><span class="sxs-lookup"><span data-stu-id="259d4-125">-Force</span></span>
<span data-ttu-id="259d4-126">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="259d4-126">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259d4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="259d4-127">-WhatIf</span></span>
<span data-ttu-id="259d4-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="259d4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="259d4-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="259d4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="259d4-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="259d4-130">-Confirm</span></span>
<span data-ttu-id="259d4-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="259d4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="259d4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="259d4-132">CommonParameters</span></span>
<span data-ttu-id="259d4-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="259d4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="259d4-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="259d4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="259d4-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="259d4-135">INPUTS</span></span>

## <span data-ttu-id="259d4-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="259d4-136">OUTPUTS</span></span>

## <span data-ttu-id="259d4-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="259d4-137">NOTES</span></span>

## <span data-ttu-id="259d4-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="259d4-138">RELATED LINKS</span></span>
