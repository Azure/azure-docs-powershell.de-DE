---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46efba5e2ab9a5c51172264b343b0f4f2b508065
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93474334"
---
# <span data-ttu-id="a20c5-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="a20c5-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="a20c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a20c5-102">SYNOPSIS</span></span>
<span data-ttu-id="a20c5-103">Lädt Azure-Authentifizierungsinformationen aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="a20c5-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="a20c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a20c5-104">SYNTAX</span></span>

### <span data-ttu-id="a20c5-105">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="a20c5-105">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a20c5-106">ProfileFromDisk</span><span class="sxs-lookup"><span data-stu-id="a20c5-106">ProfileFromDisk</span></span>
```
Import-AzureRmContext [-Path] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a20c5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a20c5-107">DESCRIPTION</span></span>
<span data-ttu-id="a20c5-108">Das Import-AzureRmContext-Cmdlet lädt Authentifizierungsinformationen aus einer Datei, um die Azure-Umgebung und den Kontext zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a20c5-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="a20c5-109">Cmdlets, die Sie in der aktuellen Sitzung ausführen, verwenden diese Informationen, um Anforderungen an den Azure Resource Manager zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="a20c5-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="a20c5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a20c5-110">EXAMPLES</span></span>

### <span data-ttu-id="a20c5-111">Beispiel 1: Importieren eines Kontexts aus einem AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="a20c5-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="a20c5-112">In diesem Beispiel wird ein Kontext aus einem PSAzureProfile-Element importiert, das an das Cmdlet übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a20c5-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="a20c5-113">Beispiel 2: Importieren eines Kontexts aus einer JSON-Datei</span><span class="sxs-lookup"><span data-stu-id="a20c5-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="a20c5-114">In diesem Beispiel wird ein Kontext aus einer JSON-Datei ausgewählt, die an das Cmdlet übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a20c5-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span>
<span data-ttu-id="a20c5-115">Diese JSON-Datei kann aus Import-AzureRmContext erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a20c5-115">This JSON file can be created from Import-AzureRmContext.</span></span>

## <span data-ttu-id="a20c5-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="a20c5-116">PARAMETERS</span></span>

### <span data-ttu-id="a20c5-117">-Azurecontext</span><span class="sxs-lookup"><span data-stu-id="a20c5-117">-AzureContext</span></span>
<span data-ttu-id="a20c5-118">Gibt den Azure-Kontext an, aus dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a20c5-118">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="a20c5-119">Wenn Sie keinen Kontext angeben, liest dieses Cmdlet aus dem lokalen Standardkontext.</span><span class="sxs-lookup"><span data-stu-id="a20c5-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a20c5-120">-Path</span><span class="sxs-lookup"><span data-stu-id="a20c5-120">-Path</span></span>
<span data-ttu-id="a20c5-121">Gibt den Pfad zu Kontextinformationen an, die mithilfe von Save-AzureRMContext gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="a20c5-121">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a20c5-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a20c5-122">-Confirm</span></span>
<span data-ttu-id="a20c5-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a20c5-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a20c5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a20c5-124">-WhatIf</span></span>
<span data-ttu-id="a20c5-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a20c5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a20c5-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a20c5-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="a20c5-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a20c5-127">INPUTS</span></span>

### <span data-ttu-id="a20c5-128">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="a20c5-128">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>
<span data-ttu-id="a20c5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a20c5-129">System.String</span></span>

## <span data-ttu-id="a20c5-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a20c5-130">OUTPUTS</span></span>

### <span data-ttu-id="a20c5-131">Microsoft. Azure. Commands. profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="a20c5-131">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="a20c5-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="a20c5-132">NOTES</span></span>

## <span data-ttu-id="a20c5-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a20c5-133">RELATED LINKS</span></span>

