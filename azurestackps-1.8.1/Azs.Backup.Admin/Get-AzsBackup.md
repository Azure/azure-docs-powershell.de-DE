---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b51280387ad3eb29f05bee8876765a621e0d07c4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828252"
---
# <span data-ttu-id="87a8a-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="87a8a-101">Get-AzsBackup</span></span>

## <span data-ttu-id="87a8a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87a8a-102">SYNOPSIS</span></span>
<span data-ttu-id="87a8a-103">Gibt eine Sicherung von einem Speicherort basierend auf dem Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="87a8a-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="87a8a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87a8a-104">SYNTAX</span></span>

### <span data-ttu-id="87a8a-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="87a8a-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="87a8a-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="87a8a-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="87a8a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="87a8a-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="87a8a-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="87a8a-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="87a8a-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87a8a-109">DESCRIPTION</span></span>
<span data-ttu-id="87a8a-110">Gibt eine Sicherung von einem Speicherort basierend auf dem Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="87a8a-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="87a8a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87a8a-111">EXAMPLES</span></span>

### <span data-ttu-id="87a8a-112">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="87a8a-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="87a8a-113">Abrufen von Informationen über alle Azure Stack-Sicherungen.</span><span class="sxs-lookup"><span data-stu-id="87a8a-113">Get information sbout all Azure Stack backups.</span></span>

### <span data-ttu-id="87a8a-114">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="87a8a-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="87a8a-115">Rufen Sie Informationen für die angegebene Azure Stack-Sicherung ab.</span><span class="sxs-lookup"><span data-stu-id="87a8a-115">Get information for the the specified Azure Stack backup.</span></span>

## <span data-ttu-id="87a8a-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="87a8a-116">PARAMETERS</span></span>

### <span data-ttu-id="87a8a-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="87a8a-117">-Location</span></span>
<span data-ttu-id="87a8a-118">Speicherort gesichert.</span><span class="sxs-lookup"><span data-stu-id="87a8a-118">Location backed up.</span></span>

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

### <span data-ttu-id="87a8a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="87a8a-119">-Name</span></span>
<span data-ttu-id="87a8a-120">Der Name der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="87a8a-120">Name of the backup.</span></span>

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

### <span data-ttu-id="87a8a-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="87a8a-121">-ParentResource</span></span>
<span data-ttu-id="87a8a-122">Durch das Übergeben eines Sicherungsspeicherorts wird die Liste aller Sicherungen an diesem Sicherungsspeicherort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="87a8a-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

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

### <span data-ttu-id="87a8a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87a8a-123">-ResourceGroupName</span></span>
<span data-ttu-id="87a8a-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="87a8a-124">Name of the resource group.</span></span>

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

### <span data-ttu-id="87a8a-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="87a8a-125">-ResourceId</span></span>
<span data-ttu-id="87a8a-126">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="87a8a-126">The resource id.</span></span>

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

### <span data-ttu-id="87a8a-127">-Skip</span><span class="sxs-lookup"><span data-stu-id="87a8a-127">-Skip</span></span>
<span data-ttu-id="87a8a-128">{{Fill Skip Description}}</span><span class="sxs-lookup"><span data-stu-id="87a8a-128">{{Fill Skip Description}}</span></span>

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

### <span data-ttu-id="87a8a-129">-Top</span><span class="sxs-lookup"><span data-stu-id="87a8a-129">-Top</span></span>
<span data-ttu-id="87a8a-130">{{Fill Top Description}}</span><span class="sxs-lookup"><span data-stu-id="87a8a-130">{{Fill Top Description}}</span></span>

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

### <span data-ttu-id="87a8a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a8a-131">CommonParameters</span></span>
<span data-ttu-id="87a8a-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87a8a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a8a-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87a8a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a8a-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87a8a-134">INPUTS</span></span>

## <span data-ttu-id="87a8a-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87a8a-135">OUTPUTS</span></span>

### <span data-ttu-id="87a8a-136">Microsoft. AzureStack. Management. Backup. admin. Models. Backup</span><span class="sxs-lookup"><span data-stu-id="87a8a-136">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="87a8a-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="87a8a-137">NOTES</span></span>

## <span data-ttu-id="87a8a-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87a8a-138">RELATED LINKS</span></span>

