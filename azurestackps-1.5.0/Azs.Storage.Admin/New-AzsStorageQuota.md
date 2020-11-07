---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 143f368b73aac490242e42f21ed76ee76ab012dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93662018"
---
# <span data-ttu-id="d50be-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="d50be-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="d50be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d50be-102">SYNOPSIS</span></span>
<span data-ttu-id="d50be-103">Erstellen Sie ein neues Speicherkontingent.</span><span class="sxs-lookup"><span data-stu-id="d50be-103">Create a new storage quota.</span></span>

## <span data-ttu-id="d50be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d50be-104">SYNTAX</span></span>

```
New-AzsStorageQuota [-Name] <String> [[-CapacityInGb] <Int32>] [[-NumberOfStorageAccounts] <Int32>]
 [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d50be-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d50be-105">DESCRIPTION</span></span>
<span data-ttu-id="d50be-106">Erstellen Sie ein neues Speicherkontingent.</span><span class="sxs-lookup"><span data-stu-id="d50be-106">Create a new storage quota.</span></span>

## <span data-ttu-id="d50be-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d50be-107">EXAMPLES</span></span>

### <span data-ttu-id="d50be-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d50be-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsStorageQuota -CapacityInGb 1000 -NumberOfStorageAccounts 100 -Name 'TestCreateStorageQuota'
```

<span data-ttu-id="d50be-109">Erstellen Sie ein neues Speicherkontingent mit angegebenen Werten.</span><span class="sxs-lookup"><span data-stu-id="d50be-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="d50be-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d50be-110">PARAMETERS</span></span>

### <span data-ttu-id="d50be-111">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="d50be-111">-CapacityInGb</span></span>
<span data-ttu-id="d50be-112">Maximal-Kapazität (GB).</span><span class="sxs-lookup"><span data-stu-id="d50be-112">Maxium capacity (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d50be-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="d50be-113">-Location</span></span>
<span data-ttu-id="d50be-114">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="d50be-114">Resource location.</span></span>

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

### <span data-ttu-id="d50be-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d50be-115">-Name</span></span>
<span data-ttu-id="d50be-116">Der Name des Speicherkontingents.</span><span class="sxs-lookup"><span data-stu-id="d50be-116">The name of the storage quota.</span></span>

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

### <span data-ttu-id="d50be-117">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="d50be-117">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="d50be-118">Gesamtzahl der Speicherkonten.</span><span class="sxs-lookup"><span data-stu-id="d50be-118">Total number of storage accounts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d50be-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d50be-119">-Confirm</span></span>
<span data-ttu-id="d50be-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d50be-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d50be-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d50be-121">-WhatIf</span></span>
<span data-ttu-id="d50be-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d50be-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d50be-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d50be-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d50be-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d50be-124">CommonParameters</span></span>
<span data-ttu-id="d50be-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d50be-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d50be-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d50be-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d50be-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d50be-127">INPUTS</span></span>

## <span data-ttu-id="d50be-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d50be-128">OUTPUTS</span></span>

### <span data-ttu-id="d50be-129">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="d50be-129">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="d50be-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="d50be-130">NOTES</span></span>

## <span data-ttu-id="d50be-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d50be-131">RELATED LINKS</span></span>

