---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: db6eff0b0b0e0698c42dd7905cd3e5f7879345e1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828328"
---
# <span data-ttu-id="8b099-101">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="8b099-101">New-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="8b099-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b099-102">SYNOPSIS</span></span>
<span data-ttu-id="8b099-103">Startet einen Auftrag für die verwaltete Datenträger Migration, um verwaltete Datenträger zur angegebenen Zielfreigabe zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="8b099-103">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

## <span data-ttu-id="8b099-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b099-104">SYNTAX</span></span>

```
New-AzsDiskMigrationJob [-Disks] <Disk[]> [-TargetShare] <String> [[-Location] <String>] [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="8b099-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b099-105">DESCRIPTION</span></span>
<span data-ttu-id="8b099-106">Erstellen eines Datenträger Migrationsauftrags</span><span class="sxs-lookup"><span data-stu-id="8b099-106">Create a disk migration job.</span></span>

## <span data-ttu-id="8b099-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b099-107">EXAMPLES</span></span>

### <span data-ttu-id="8b099-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8b099-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsDiskMigrationJob -Name "MyMigrationJob" -Disks $disks -location local -TargetShare "\\SU1FileServer.azurestack.local\SU1_ObjStore"
```

<span data-ttu-id="8b099-109">Starten eines verwalteten Datenträger Migrationsauftrags für die ersten 20 Datenträger</span><span class="sxs-lookup"><span data-stu-id="8b099-109">Start a managed disk migration job for the first 20 disks</span></span>

## <span data-ttu-id="8b099-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b099-110">PARAMETERS</span></span>

### <span data-ttu-id="8b099-111">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="8b099-111">-Disks</span></span>
<span data-ttu-id="8b099-112">Die Parameter der Datenträgerliste.</span><span class="sxs-lookup"><span data-stu-id="8b099-112">The parameters of disk list.</span></span>

```yaml
Type: Disk[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b099-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="8b099-113">-Location</span></span>
<span data-ttu-id="8b099-114">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="8b099-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b099-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8b099-115">-Name</span></span>
<span data-ttu-id="8b099-116">Der GUID-Name des Migrationsauftrags.</span><span class="sxs-lookup"><span data-stu-id="8b099-116">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b099-117">-TargetShare</span><span class="sxs-lookup"><span data-stu-id="8b099-117">-TargetShare</span></span>
<span data-ttu-id="8b099-118">Der Name der Zielfreigabe.</span><span class="sxs-lookup"><span data-stu-id="8b099-118">The target share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b099-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b099-119">CommonParameters</span></span>
<span data-ttu-id="8b099-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b099-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b099-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b099-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b099-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b099-122">INPUTS</span></span>

## <span data-ttu-id="8b099-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b099-123">OUTPUTS</span></span>

### <span data-ttu-id="8b099-124">Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="8b099-124">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="8b099-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b099-125">NOTES</span></span>

## <span data-ttu-id="8b099-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b099-126">RELATED LINKS</span></span>

