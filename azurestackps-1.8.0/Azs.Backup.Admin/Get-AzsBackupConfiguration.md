---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25091f0cb439e0447d19b534d59a0084a5b05c6e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827944"
---
# <span data-ttu-id="e9b37-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9b37-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="e9b37-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e9b37-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b37-103">Gibt die Liste der Sicherungs Konfigurationen zurück.</span><span class="sxs-lookup"><span data-stu-id="e9b37-103">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="e9b37-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9b37-104">SYNTAX</span></span>

### <span data-ttu-id="e9b37-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="e9b37-105">List (Default)</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e9b37-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="e9b37-106">Get</span></span>
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="e9b37-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9b37-107">ResourceId</span></span>
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e9b37-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9b37-108">DESCRIPTION</span></span>
<span data-ttu-id="e9b37-109">Gibt die Liste der Sicherungs Konfigurationen zurück.</span><span class="sxs-lookup"><span data-stu-id="e9b37-109">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="e9b37-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9b37-110">EXAMPLES</span></span>

### <span data-ttu-id="e9b37-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e9b37-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackupConfiguration
```

<span data-ttu-id="e9b37-112">Erhalten Sie die Azure Stack-Sicherungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e9b37-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="e9b37-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9b37-113">PARAMETERS</span></span>

### <span data-ttu-id="e9b37-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="e9b37-114">-Location</span></span>
<span data-ttu-id="e9b37-115">Sicherungsspeicherort.</span><span class="sxs-lookup"><span data-stu-id="e9b37-115">Backup location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b37-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9b37-116">-ResourceGroupName</span></span>
<span data-ttu-id="e9b37-117">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e9b37-117">Name of the resource group.</span></span>

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

### <span data-ttu-id="e9b37-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e9b37-118">-ResourceId</span></span>
<span data-ttu-id="e9b37-119">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="e9b37-119">The resource id.</span></span>

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

### <span data-ttu-id="e9b37-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="e9b37-120">-Skip</span></span>
<span data-ttu-id="e9b37-121">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="e9b37-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b37-122">-Top</span><span class="sxs-lookup"><span data-stu-id="e9b37-122">-Top</span></span>
<span data-ttu-id="e9b37-123">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="e9b37-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e9b37-124">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="e9b37-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b37-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b37-125">CommonParameters</span></span>
<span data-ttu-id="e9b37-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9b37-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b37-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9b37-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b37-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e9b37-128">INPUTS</span></span>

## <span data-ttu-id="e9b37-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e9b37-129">OUTPUTS</span></span>

### <span data-ttu-id="e9b37-130">Microsoft. AzureStack. Management. Backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="e9b37-130">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="e9b37-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="e9b37-131">NOTES</span></span>

## <span data-ttu-id="e9b37-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e9b37-132">RELATED LINKS</span></span>

