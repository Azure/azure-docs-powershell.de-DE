---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54016a200b4304c7e37777202a8450fc9ad10e1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650529"
---
# <span data-ttu-id="94ed7-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="94ed7-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="94ed7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="94ed7-103">Startet einen Container Migrationsauftrag zum Migrieren von Containern zur angegebenen Zielfreigabe.</span><span class="sxs-lookup"><span data-stu-id="94ed7-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="94ed7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94ed7-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-Name] <String> [-ShareName] <String>
 [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94ed7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94ed7-105">DESCRIPTION</span></span>
<span data-ttu-id="94ed7-106">Startet einen Container Migrationsauftrag zum Migrieren von Containern zur angegebenen Zielfreigabe.</span><span class="sxs-lookup"><span data-stu-id="94ed7-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="94ed7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94ed7-107">EXAMPLES</span></span>

### <span data-ttu-id="94ed7-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="94ed7-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -Name "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="94ed7-109">Startet eine Container Migration.</span><span class="sxs-lookup"><span data-stu-id="94ed7-109">Starts a container migration.</span></span>

## <span data-ttu-id="94ed7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="94ed7-110">PARAMETERS</span></span>

### <span data-ttu-id="94ed7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94ed7-111">-AsJob</span></span>
<span data-ttu-id="94ed7-112">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="94ed7-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="94ed7-113">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="94ed7-113">-DestinationShareUncPath</span></span>
<span data-ttu-id="94ed7-114">Der UNC-Pfad der Zielfreigabe für die Migration.</span><span class="sxs-lookup"><span data-stu-id="94ed7-114">The UNC path of the destination share for migration.</span></span>

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

### <span data-ttu-id="94ed7-115">-Farmname</span><span class="sxs-lookup"><span data-stu-id="94ed7-115">-FarmName</span></span>
<span data-ttu-id="94ed7-116">Farm-ID.</span><span class="sxs-lookup"><span data-stu-id="94ed7-116">Farm Id.</span></span>

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

### <span data-ttu-id="94ed7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="94ed7-117">-Force</span></span>
<span data-ttu-id="94ed7-118">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="94ed7-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="94ed7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="94ed7-119">-Name</span></span>
<span data-ttu-id="94ed7-120">Der Name des zu migrierenden Containers.</span><span class="sxs-lookup"><span data-stu-id="94ed7-120">The name of the container to be migrated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ed7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94ed7-121">-ResourceGroupName</span></span>
<span data-ttu-id="94ed7-122">Der Name der Ressourcengruppe, unter der der Speicherressourcen Anbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="94ed7-122">The resource group name in which the storage resource provider was registered under.</span></span>

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

### <span data-ttu-id="94ed7-123">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="94ed7-123">-ShareName</span></span>
<span data-ttu-id="94ed7-124">Der Name der Freigabe, die den für die Migration angegebenen Container enthält.</span><span class="sxs-lookup"><span data-stu-id="94ed7-124">Name of the share containing the container specified for migration.</span></span>

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

### <span data-ttu-id="94ed7-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="94ed7-125">-StorageAccountName</span></span>
<span data-ttu-id="94ed7-126">Der Name des speicherkontos, in dem der Container gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="94ed7-126">The name of storage account where the container locates.</span></span>

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

### <span data-ttu-id="94ed7-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="94ed7-127">-Confirm</span></span>
<span data-ttu-id="94ed7-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="94ed7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94ed7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94ed7-129">-WhatIf</span></span>
<span data-ttu-id="94ed7-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94ed7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94ed7-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94ed7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94ed7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ed7-132">CommonParameters</span></span>
<span data-ttu-id="94ed7-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94ed7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ed7-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94ed7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ed7-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94ed7-135">INPUTS</span></span>

## <span data-ttu-id="94ed7-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94ed7-136">OUTPUTS</span></span>

## <span data-ttu-id="94ed7-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="94ed7-137">NOTES</span></span>

## <span data-ttu-id="94ed7-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94ed7-138">RELATED LINKS</span></span>

