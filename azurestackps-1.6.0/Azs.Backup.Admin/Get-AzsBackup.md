---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb306ed03cb9ab1f06209345474b2ef196d9e1d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475590"
---
# <span data-ttu-id="42444-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="42444-101">Get-AzsBackup</span></span>

## <span data-ttu-id="42444-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42444-102">SYNOPSIS</span></span>
<span data-ttu-id="42444-103">Gibt eine Sicherung von einem Speicherort basierend auf dem Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="42444-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="42444-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42444-104">SYNTAX</span></span>

### <span data-ttu-id="42444-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="42444-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="42444-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="42444-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="42444-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="42444-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="42444-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="42444-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="42444-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42444-109">DESCRIPTION</span></span>
<span data-ttu-id="42444-110">Gibt eine Sicherung von einem Speicherort basierend auf dem Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="42444-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="42444-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42444-111">EXAMPLES</span></span>

### <span data-ttu-id="42444-112">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="42444-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="42444-113">Abrufen von Informationen zu allen Azure Stack-Sicherungen</span><span class="sxs-lookup"><span data-stu-id="42444-113">Get information about all Azure Stack backups.</span></span>

### <span data-ttu-id="42444-114">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="42444-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="42444-115">Abrufen von Informationen für die angegebene Azure Stack-Sicherung</span><span class="sxs-lookup"><span data-stu-id="42444-115">Get information for the specified Azure Stack backup.</span></span>

## <span data-ttu-id="42444-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="42444-116">PARAMETERS</span></span>

### <span data-ttu-id="42444-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="42444-117">-Location</span></span>
<span data-ttu-id="42444-118">Speicherort gesichert.</span><span class="sxs-lookup"><span data-stu-id="42444-118">Location backed up.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42444-119">-Name</span><span class="sxs-lookup"><span data-stu-id="42444-119">-Name</span></span>
<span data-ttu-id="42444-120">Der Name der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="42444-120">Name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42444-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="42444-121">-ParentResource</span></span>
<span data-ttu-id="42444-122">Durch das Übergeben eines Sicherungsspeicherorts wird die Liste aller Sicherungen an diesem Sicherungsspeicherort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="42444-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

```yaml
Type: BackupLocation
Parameter Sets: ParentResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42444-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42444-123">-ResourceGroupName</span></span>
<span data-ttu-id="42444-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="42444-124">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42444-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="42444-125">-ResourceId</span></span>
<span data-ttu-id="42444-126">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="42444-126">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42444-127">-Skip</span><span class="sxs-lookup"><span data-stu-id="42444-127">-Skip</span></span>
<span data-ttu-id="42444-128">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="42444-128">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List, ParentResource
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42444-129">-Top</span><span class="sxs-lookup"><span data-stu-id="42444-129">-Top</span></span>
<span data-ttu-id="42444-130">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="42444-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="42444-131">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="42444-131">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List, ParentResource
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42444-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42444-132">CommonParameters</span></span>
<span data-ttu-id="42444-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42444-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42444-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42444-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42444-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42444-135">INPUTS</span></span>

## <span data-ttu-id="42444-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42444-136">OUTPUTS</span></span>

### <span data-ttu-id="42444-137">Microsoft. AzureStack. Management. Backup. admin. Models. Backup</span><span class="sxs-lookup"><span data-stu-id="42444-137">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="42444-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="42444-138">NOTES</span></span>

## <span data-ttu-id="42444-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42444-139">RELATED LINKS</span></span>

