---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
ms.openlocfilehash: bb1f34a27d9f1ad5d8e851cd280751c25ebf25c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496957"
---
# <span data-ttu-id="aa12f-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="aa12f-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="aa12f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aa12f-102">SYNOPSIS</span></span>
<span data-ttu-id="aa12f-103">Lädt Azure-Authentifizierungsinformationen aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="aa12f-103">Loads Azure authentication information from a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa12f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa12f-104">SYNTAX</span></span>

### <span data-ttu-id="aa12f-105">ProfileFromDisk (Standard)</span><span class="sxs-lookup"><span data-stu-id="aa12f-105">ProfileFromDisk (Default)</span></span>
```
Import-AzureRmContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa12f-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="aa12f-106">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa12f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa12f-107">DESCRIPTION</span></span>
<span data-ttu-id="aa12f-108">Das Import-AzureRmContext-Cmdlet lädt Authentifizierungsinformationen aus einer Datei, um die Azure-Umgebung und den Kontext zu definieren.</span><span class="sxs-lookup"><span data-stu-id="aa12f-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="aa12f-109">Cmdlets, die Sie in der aktuellen Sitzung ausführen, verwenden diese Informationen, um Anforderungen an den Azure Resource Manager zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="aa12f-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="aa12f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa12f-110">EXAMPLES</span></span>

### <span data-ttu-id="aa12f-111">Beispiel 1: Importieren eines Kontexts aus einem AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="aa12f-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="aa12f-112">In diesem Beispiel wird ein Kontext aus einem PSAzureProfile-Element importiert, das an das Cmdlet übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="aa12f-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="aa12f-113">Beispiel 2: Importieren eines Kontexts aus einer JSON-Datei</span><span class="sxs-lookup"><span data-stu-id="aa12f-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="aa12f-114">In diesem Beispiel wird ein Kontext aus einer JSON-Datei ausgewählt, die an das Cmdlet übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="aa12f-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="aa12f-115">Diese JSON-Datei kann aus Save-AzureRmContext erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="aa12f-115">This JSON file can be created from Save-AzureRmContext.</span></span>

## <span data-ttu-id="aa12f-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa12f-116">PARAMETERS</span></span>

### <span data-ttu-id="aa12f-117">-Azurecontext</span><span class="sxs-lookup"><span data-stu-id="aa12f-117">-AzureContext</span></span>
<span data-ttu-id="aa12f-118">Gibt den Azure-Kontext an, aus dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="aa12f-118">Specifies the Azure context from which this cmdlet reads.</span></span> <span data-ttu-id="aa12f-119">Wenn Sie keinen Kontext angeben, liest dieses Cmdlet aus dem lokalen Standardkontext.</span><span class="sxs-lookup"><span data-stu-id="aa12f-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa12f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa12f-120">-DefaultProfile</span></span>
<span data-ttu-id="aa12f-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="aa12f-121">The credentials, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa12f-122">-Path</span><span class="sxs-lookup"><span data-stu-id="aa12f-122">-Path</span></span>
<span data-ttu-id="aa12f-123">Gibt den Pfad zu Kontextinformationen an, die mithilfe von Save-AzureRMContext gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="aa12f-123">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: System.String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa12f-124">-Scope</span><span class="sxs-lookup"><span data-stu-id="aa12f-124">-Scope</span></span>
<span data-ttu-id="aa12f-125">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="aa12f-125">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa12f-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aa12f-126">-Confirm</span></span>
<span data-ttu-id="aa12f-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa12f-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa12f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa12f-128">-WhatIf</span></span>
<span data-ttu-id="aa12f-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa12f-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa12f-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa12f-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa12f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa12f-131">CommonParameters</span></span>
<span data-ttu-id="aa12f-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa12f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa12f-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa12f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa12f-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aa12f-134">INPUTS</span></span>

### <span data-ttu-id="aa12f-135">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="aa12f-135">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>
<span data-ttu-id="aa12f-136">Enthält den Satz von Anmeldeinformationen, Konten und Abonnements, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa12f-136">Contains the set of credentials, accounts, and subscriptions that are used to communicate with Azure.</span></span>

## <span data-ttu-id="aa12f-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aa12f-137">OUTPUTS</span></span>

### <span data-ttu-id="aa12f-138">Microsoft. Azure. Commands. profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="aa12f-138">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>
<span data-ttu-id="aa12f-139">Enthält den Satz von Anmeldeinformationen, Konten und Abonnements, die für die Kommunikation mit Azure verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="aa12f-139">Contains the set of credentials, accounts, and subscriptions that can be used to communicate with Azure.</span></span>

## <span data-ttu-id="aa12f-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="aa12f-140">NOTES</span></span>

## <span data-ttu-id="aa12f-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aa12f-141">RELATED LINKS</span></span>

