---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20b70e2eeb1aa2d98f595dfe7bbe3075174c1f64
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827507"
---
# <span data-ttu-id="4cb82-101">New-DirectoryTenantObject</span><span class="sxs-lookup"><span data-stu-id="4cb82-101">New-DirectoryTenantObject</span></span>

## <span data-ttu-id="4cb82-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4cb82-102">SYNOPSIS</span></span>
<span data-ttu-id="4cb82-103">Verzeichnis Mandant.</span><span class="sxs-lookup"><span data-stu-id="4cb82-103">Directory tenant.</span></span>

## <span data-ttu-id="4cb82-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cb82-104">SYNTAX</span></span>

```
New-DirectoryTenantObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-Name] <String>]
 [[-TenantId] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="4cb82-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4cb82-105">DESCRIPTION</span></span>
<span data-ttu-id="4cb82-106">Verzeichnis Mandant.</span><span class="sxs-lookup"><span data-stu-id="4cb82-106">Directory tenant.</span></span>

## <span data-ttu-id="4cb82-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4cb82-107">EXAMPLES</span></span>

### <span data-ttu-id="4cb82-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4cb82-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="4cb82-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="4cb82-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="4cb82-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cb82-110">PARAMETERS</span></span>

### <span data-ttu-id="4cb82-111">-ID</span><span class="sxs-lookup"><span data-stu-id="4cb82-111">-Id</span></span>
<span data-ttu-id="4cb82-112">Der URI der Ressource.</span><span class="sxs-lookup"><span data-stu-id="4cb82-112">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb82-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="4cb82-113">-Location</span></span>
<span data-ttu-id="4cb82-114">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="4cb82-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb82-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4cb82-115">-Name</span></span>
<span data-ttu-id="4cb82-116">Der Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="4cb82-116">Name of the resource.</span></span>

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

### <span data-ttu-id="4cb82-117">-Tags</span><span class="sxs-lookup"><span data-stu-id="4cb82-117">-Tags</span></span>
<span data-ttu-id="4cb82-118">Liste der Schlüssel-Wert-Paare</span><span class="sxs-lookup"><span data-stu-id="4cb82-118">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb82-119">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="4cb82-119">-TenantId</span></span>
<span data-ttu-id="4cb82-120">Eindeutige Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="4cb82-120">Tenant unique identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb82-121">-Typ</span><span class="sxs-lookup"><span data-stu-id="4cb82-121">-Type</span></span>
<span data-ttu-id="4cb82-122">Der Typ der Ressource.</span><span class="sxs-lookup"><span data-stu-id="4cb82-122">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb82-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cb82-123">CommonParameters</span></span>
<span data-ttu-id="4cb82-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cb82-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cb82-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cb82-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cb82-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4cb82-126">INPUTS</span></span>

## <span data-ttu-id="4cb82-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4cb82-127">OUTPUTS</span></span>

## <span data-ttu-id="4cb82-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="4cb82-128">NOTES</span></span>

## <span data-ttu-id="4cb82-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4cb82-129">RELATED LINKS</span></span>

