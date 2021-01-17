---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
ms.openlocfilehash: 2c7ba44358db4e6a578f9876e26a099b2242badc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469187"
---
# <span data-ttu-id="44071-101">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="44071-101">Remove-AzEnvironment</span></span>

## <span data-ttu-id="44071-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44071-102">SYNOPSIS</span></span>
<span data-ttu-id="44071-103">Entfernt Endpunkte und Metadaten zum Herstellen einer Verbindung mit einer bestimmten Azure-Instanz.</span><span class="sxs-lookup"><span data-stu-id="44071-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="44071-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44071-104">SYNTAX</span></span>

```
Remove-AzEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44071-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44071-105">DESCRIPTION</span></span>
<span data-ttu-id="44071-106">Das Remove-AzEnvironment cmdlet entfernt Endpunkte und Metadateninformationen zum Herstellen einer Verbindung mit einer bestimmten Azure-Instanz.</span><span class="sxs-lookup"><span data-stu-id="44071-106">The Remove-AzEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="44071-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="44071-107">EXAMPLES</span></span>

### <span data-ttu-id="44071-108">Beispiel 1: Erstellen und Entfernen einer Testumgebung</span><span class="sxs-lookup"><span data-stu-id="44071-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Remove-AzEnvironment -Name TestEnvironment

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="44071-109">In diesem Beispiel wird gezeigt, wie Sie mit "Add-AzEnvironment" eine Umgebung erstellen und dann die Umgebung mit "Remove-AzEnvironment" löschen.</span><span class="sxs-lookup"><span data-stu-id="44071-109">This example shows how to create an environment using Add-AzEnvironment, and then how to delete the environment using Remove-AzEnvironment.</span></span>

## <span data-ttu-id="44071-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44071-110">PARAMETERS</span></span>

### <span data-ttu-id="44071-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44071-111">-DefaultProfile</span></span>
<span data-ttu-id="44071-112">Die Anmeldeinformationen, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44071-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44071-113">-Name</span><span class="sxs-lookup"><span data-stu-id="44071-113">-Name</span></span>
<span data-ttu-id="44071-114">Gibt den Namen der zu entfernenden Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="44071-114">Specifies the name of the environment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44071-115">-Scope</span><span class="sxs-lookup"><span data-stu-id="44071-115">-Scope</span></span>
<span data-ttu-id="44071-116">Bestimmt den Umfang von Kontextänderungen, z. B. ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="44071-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="44071-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44071-117">-Confirm</span></span>
<span data-ttu-id="44071-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="44071-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44071-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="44071-119">-WhatIf</span></span>
<span data-ttu-id="44071-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44071-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44071-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44071-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44071-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44071-122">CommonParameters</span></span>
<span data-ttu-id="44071-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44071-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44071-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44071-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44071-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="44071-125">INPUTS</span></span>

### <span data-ttu-id="44071-126">System.String</span><span class="sxs-lookup"><span data-stu-id="44071-126">System.String</span></span>

## <span data-ttu-id="44071-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="44071-127">OUTPUTS</span></span>

### <span data-ttu-id="44071-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="44071-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="44071-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="44071-129">NOTES</span></span>

## <span data-ttu-id="44071-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="44071-130">RELATED LINKS</span></span>

[<span data-ttu-id="44071-131">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="44071-131">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="44071-132">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="44071-132">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="44071-133">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="44071-133">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

