---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/import-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
ms.openlocfilehash: 40d5cef72a8a1f345ac7f6389bacfb75257ccab4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157697"
---
# <span data-ttu-id="258ef-101">Import-AzContext</span><span class="sxs-lookup"><span data-stu-id="258ef-101">Import-AzContext</span></span>

## <span data-ttu-id="258ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="258ef-102">SYNOPSIS</span></span>
<span data-ttu-id="258ef-103">Lädt die Azure-Authentifizierungsinformationen aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="258ef-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="258ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="258ef-104">SYNTAX</span></span>

### <span data-ttu-id="258ef-105">ProfileFromDisk (Standard)</span><span class="sxs-lookup"><span data-stu-id="258ef-105">ProfileFromDisk (Default)</span></span>
```
Import-AzContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="258ef-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="258ef-106">InMemoryProfile</span></span>
```
Import-AzContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="258ef-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="258ef-107">DESCRIPTION</span></span>
<span data-ttu-id="258ef-108">Das Import-AzContext lädt Authentifizierungsinformationen aus einer Datei, um die Umgebung und den Kontext von Azure festlegen.</span><span class="sxs-lookup"><span data-stu-id="258ef-108">The Import-AzContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="258ef-109">Cmdlets, die Sie in der aktuellen Sitzung ausführen, verwenden diese Informationen, um Anforderungen an Azure Resource Manager zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="258ef-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="258ef-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="258ef-110">EXAMPLES</span></span>

### <span data-ttu-id="258ef-111">Beispiel 1: Importieren eines Kontexts aus AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="258ef-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzContext -AzContext (Connect-AzAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="258ef-112">In diesem Beispiel wird ein Kontext aus einem PSAzureProfile importiert, der an das Cmdlet übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="258ef-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="258ef-113">Beispiel 2: Importieren eines Kontexts aus einer JSON-Datei</span><span class="sxs-lookup"><span data-stu-id="258ef-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="258ef-114">In diesem Beispiel wird ein Kontext aus einer JSON-Datei ausgewählt, der an das Cmdlet übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="258ef-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="258ef-115">Diese JSON-Datei kann aus Save-AzContext erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="258ef-115">This JSON file can be created from Save-AzContext.</span></span>

## <span data-ttu-id="258ef-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="258ef-116">PARAMETERS</span></span>

### <span data-ttu-id="258ef-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="258ef-117">-AzureContext</span></span>
<span data-ttu-id="258ef-118">{{Fill AzureContext Description}}</span><span class="sxs-lookup"><span data-stu-id="258ef-118">{{Fill AzureContext Description}}</span></span>

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

### <span data-ttu-id="258ef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="258ef-119">-DefaultProfile</span></span>
<span data-ttu-id="258ef-120">Die Anmeldeinformationen, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="258ef-120">The credentials, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="258ef-121">-Path</span><span class="sxs-lookup"><span data-stu-id="258ef-121">-Path</span></span>
<span data-ttu-id="258ef-122">Gibt den Pfad zu Kontextinformationen an, die mit Save-AzContext gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="258ef-122">Specifies the path to context information saved by using Save-AzContext.</span></span>

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

### <span data-ttu-id="258ef-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="258ef-123">-Scope</span></span>
<span data-ttu-id="258ef-124">Bestimmt den Umfang von Kontextänderungen, z. B. ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="258ef-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="258ef-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="258ef-125">-Confirm</span></span>
<span data-ttu-id="258ef-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="258ef-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="258ef-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="258ef-127">-WhatIf</span></span>
<span data-ttu-id="258ef-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="258ef-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="258ef-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="258ef-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="258ef-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="258ef-130">CommonParameters</span></span>
<span data-ttu-id="258ef-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="258ef-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="258ef-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="258ef-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="258ef-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="258ef-133">INPUTS</span></span>

### <span data-ttu-id="258ef-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="258ef-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="258ef-135">System.String</span><span class="sxs-lookup"><span data-stu-id="258ef-135">System.String</span></span>

## <span data-ttu-id="258ef-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="258ef-136">OUTPUTS</span></span>

### <span data-ttu-id="258ef-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="258ef-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="258ef-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="258ef-138">NOTES</span></span>

## <span data-ttu-id="258ef-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="258ef-139">RELATED LINKS</span></span>
