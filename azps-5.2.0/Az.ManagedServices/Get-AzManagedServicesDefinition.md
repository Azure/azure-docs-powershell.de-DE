---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: 5282b3d0ae145088cf07040520050937f8d3a335
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289937"
---
# <span data-ttu-id="e1dd3-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="e1dd3-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="e1dd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1dd3-102">SYNOPSIS</span></span>
<span data-ttu-id="e1dd3-103">Ruft eine bestimmte Registrierungsdefinition oder eine Liste der Registrierungsdefinitionen ab.</span><span class="sxs-lookup"><span data-stu-id="e1dd3-103">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="e1dd3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1dd3-104">SYNTAX</span></span>

### <span data-ttu-id="e1dd3-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e1dd3-105">ByName (Default)</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1dd3-106">Standard</span><span class="sxs-lookup"><span data-stu-id="e1dd3-106">Default</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1dd3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1dd3-107">DESCRIPTION</span></span>
<span data-ttu-id="e1dd3-108">Ruft eine bestimmte Registrierungsdefinition oder eine Liste der Registrierungsdefinitionen ab.</span><span class="sxs-lookup"><span data-stu-id="e1dd3-108">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="e1dd3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e1dd3-109">EXAMPLES</span></span>

### <span data-ttu-id="e1dd3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e1dd3-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesDefinition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="e1dd3-111">Ruft alle Registrierungsdefinitionen im Standardbereich ab.</span><span class="sxs-lookup"><span data-stu-id="e1dd3-111">Gets all registration definitions at default scope.</span></span>

### <span data-ttu-id="e1dd3-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e1dd3-112">Example 2</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="e1dd3-113">Ruft die Registrierungsdefinition nach Name im Standardbereich ab.</span><span class="sxs-lookup"><span data-stu-id="e1dd3-113">Gets the registration definition by name at default scope.</span></span>

### <span data-ttu-id="e1dd3-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e1dd3-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="e1dd3-115">Ruft alle Registrierungsdefinitionen im angegebenen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="e1dd3-115">Gets all registration definitions at the given scope.</span></span>

## <span data-ttu-id="e1dd3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1dd3-116">PARAMETERS</span></span>

### <span data-ttu-id="e1dd3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1dd3-117">-DefaultProfile</span></span>
<span data-ttu-id="e1dd3-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1dd3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1dd3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e1dd3-119">-Name</span></span>
<span data-ttu-id="e1dd3-120">Der eindeutige Name der Registrierungsdefinition.</span><span class="sxs-lookup"><span data-stu-id="e1dd3-120">The unique name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1dd3-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="e1dd3-121">-Scope</span></span>
<span data-ttu-id="e1dd3-122">Der Bereich, in dem die Registrierungsdefinition erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e1dd3-122">The scope where the registration definition created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1dd3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1dd3-123">CommonParameters</span></span>
<span data-ttu-id="e1dd3-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1dd3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1dd3-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1dd3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1dd3-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e1dd3-126">INPUTS</span></span>

### <span data-ttu-id="e1dd3-127">Keine</span><span class="sxs-lookup"><span data-stu-id="e1dd3-127">None</span></span>
## <span data-ttu-id="e1dd3-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e1dd3-128">OUTPUTS</span></span>

### <span data-ttu-id="e1dd3-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="e1dd3-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="e1dd3-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e1dd3-130">NOTES</span></span>

## <span data-ttu-id="e1dd3-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e1dd3-131">RELATED LINKS</span></span>
