---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 8aae61e163baf95cbed62ea239c7d1a6190aed1f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154716"
---
# <span data-ttu-id="1d901-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="1d901-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="1d901-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d901-102">SYNOPSIS</span></span>
<span data-ttu-id="1d901-103">Ruft eine bestimmte Registrierungszuweisung oder eine Liste der Registrierungszuweisungen ab.</span><span class="sxs-lookup"><span data-stu-id="1d901-103">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="1d901-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d901-104">SYNTAX</span></span>

### <span data-ttu-id="1d901-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="1d901-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d901-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1d901-106">ByName</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-Name <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d901-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d901-107">DESCRIPTION</span></span>
<span data-ttu-id="1d901-108">Ruft eine bestimmte Registrierungszuweisung oder eine Liste der Registrierungszuweisungen ab.</span><span class="sxs-lookup"><span data-stu-id="1d901-108">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="1d901-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1d901-109">EXAMPLES</span></span>

### <span data-ttu-id="1d901-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1d901-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesAssignment

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="1d901-111">Ruft alle Registrierungszuweisungen unter dem Standardbereich ab.</span><span class="sxs-lookup"><span data-stu-id="1d901-111">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="1d901-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1d901-112">Example 2</span></span>
```
PS C:\> $assignments = Get-AzManagedServicesAssignment -ExpandRegistrationDefinition
PS C:\> $assignments[0].Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : 0c146106-c927-4098-a7ca-30bbcf44a502

PS C:\>
```

<span data-ttu-id="1d901-113">Ruft alle Registrierungszuweisungen mit den Registrierungsdefinitionsdetails ab.</span><span class="sxs-lookup"><span data-stu-id="1d901-113">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="1d901-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="1d901-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="1d901-115">Ruft eine Registrierungszuweisung nach Name ohne Registrierungsdefinitionsdetails ab.</span><span class="sxs-lookup"><span data-stu-id="1d901-115">Gets a registration assignment by name without registration definition details.</span></span>

### <span data-ttu-id="1d901-116">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="1d901-116">Example 4</span></span>
```
PS C:\> $assignment = Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80 -ExpandRegistrationDefinition
PS C:\> $assignment.Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : 0c146106-c927-4098-a7ca-30bbcf44a502

PS C:\>
```

<span data-ttu-id="1d901-117">Ruft eine Registrierungszuweisung nach Name mit Details zur Registrierungsdefinition ab.</span><span class="sxs-lookup"><span data-stu-id="1d901-117">Gets a registration assignment by name with registration definition details.</span></span>

### <span data-ttu-id="1d901-118">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="1d901-118">Example 5</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="1d901-119">Ruft alle Registrierungszuweisungen zu einem bestimmten Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="1d901-119">Gets all the registration assignments at given scope.</span></span>

## <span data-ttu-id="1d901-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d901-120">PARAMETERS</span></span>

### <span data-ttu-id="1d901-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d901-121">-DefaultProfile</span></span>
<span data-ttu-id="1d901-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d901-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d901-123">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="1d901-123">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="1d901-124">Angaben zur Registrierungsdefinition</span><span class="sxs-lookup"><span data-stu-id="1d901-124">Whether to include registration definition details.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d901-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1d901-125">-Name</span></span>
<span data-ttu-id="1d901-126">Der eindeutige Name der Registrierungszuordnung.</span><span class="sxs-lookup"><span data-stu-id="1d901-126">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="1d901-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="1d901-127">-Scope</span></span>
<span data-ttu-id="1d901-128">Der Bereich, in dem die Registrierungszuordnung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1d901-128">The scope where the registration assignment created.</span></span>

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

### <span data-ttu-id="1d901-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d901-129">CommonParameters</span></span>
<span data-ttu-id="1d901-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d901-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d901-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d901-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d901-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1d901-132">INPUTS</span></span>

### <span data-ttu-id="1d901-133">Keine</span><span class="sxs-lookup"><span data-stu-id="1d901-133">None</span></span>
## <span data-ttu-id="1d901-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1d901-134">OUTPUTS</span></span>

### <span data-ttu-id="1d901-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="1d901-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="1d901-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1d901-136">NOTES</span></span>

## <span data-ttu-id="1d901-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1d901-137">RELATED LINKS</span></span>
