---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 8aae61e163baf95cbed62ea239c7d1a6190aed1f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177546"
---
# <span data-ttu-id="fba5f-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="fba5f-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="fba5f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fba5f-102">SYNOPSIS</span></span>
<span data-ttu-id="fba5f-103">Ruft eine bestimmte Registrierungs Aufgabe oder eine Liste der Registrierungsaufgaben ab.</span><span class="sxs-lookup"><span data-stu-id="fba5f-103">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="fba5f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fba5f-104">SYNTAX</span></span>

### <span data-ttu-id="fba5f-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="fba5f-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fba5f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fba5f-106">ByName</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-Name <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fba5f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fba5f-107">DESCRIPTION</span></span>
<span data-ttu-id="fba5f-108">Ruft eine bestimmte Registrierungs Aufgabe oder eine Liste der Registrierungsaufgaben ab.</span><span class="sxs-lookup"><span data-stu-id="fba5f-108">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="fba5f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fba5f-109">EXAMPLES</span></span>

### <span data-ttu-id="fba5f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fba5f-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesAssignment

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="fba5f-111">Ruft alle Registrierungsaufgaben unter dem Standardbereich ab.</span><span class="sxs-lookup"><span data-stu-id="fba5f-111">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="fba5f-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fba5f-112">Example 2</span></span>
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

<span data-ttu-id="fba5f-113">Ruft alle Registrierungsaufgaben mit den Details der Registrierungs Definition ab.</span><span class="sxs-lookup"><span data-stu-id="fba5f-113">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="fba5f-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fba5f-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="fba5f-115">Ruft eine Registrierungs Aufgabe nach Namen ohne Details der Registrierungs Definition ab.</span><span class="sxs-lookup"><span data-stu-id="fba5f-115">Gets a registration assignment by name without registration definition details.</span></span>

### <span data-ttu-id="fba5f-116">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="fba5f-116">Example 4</span></span>
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

<span data-ttu-id="fba5f-117">Ruft eine Registrierungs Aufgabe nach Namen mit Details zur Registrierungs Definition ab.</span><span class="sxs-lookup"><span data-stu-id="fba5f-117">Gets a registration assignment by name with registration definition details.</span></span>

### <span data-ttu-id="fba5f-118">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="fba5f-118">Example 5</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="fba5f-119">Ruft alle Registrierungsaufgaben im angegebenen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="fba5f-119">Gets all the registration assignments at given scope.</span></span>

## <span data-ttu-id="fba5f-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="fba5f-120">PARAMETERS</span></span>

### <span data-ttu-id="fba5f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fba5f-121">-DefaultProfile</span></span>
<span data-ttu-id="fba5f-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fba5f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fba5f-123">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="fba5f-123">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="fba5f-124">Gibt an, ob Details zur Registrierungs Definition eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fba5f-124">Whether to include registration definition details.</span></span>

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

### <span data-ttu-id="fba5f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fba5f-125">-Name</span></span>
<span data-ttu-id="fba5f-126">Der eindeutige Name der Registrierungs Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="fba5f-126">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="fba5f-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="fba5f-127">-Scope</span></span>
<span data-ttu-id="fba5f-128">Der Bereich, in dem die Registrierungs Aufgabe erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="fba5f-128">The scope where the registration assignment created.</span></span>

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

### <span data-ttu-id="fba5f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fba5f-129">CommonParameters</span></span>
<span data-ttu-id="fba5f-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fba5f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fba5f-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fba5f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fba5f-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fba5f-132">INPUTS</span></span>

### <span data-ttu-id="fba5f-133">Keine</span><span class="sxs-lookup"><span data-stu-id="fba5f-133">None</span></span>
## <span data-ttu-id="fba5f-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fba5f-134">OUTPUTS</span></span>

### <span data-ttu-id="fba5f-135">Microsoft. Azure. PowerShell. Cmdlets. ManagedServices. Models. PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="fba5f-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="fba5f-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="fba5f-136">NOTES</span></span>

## <span data-ttu-id="fba5f-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fba5f-137">RELATED LINKS</span></span>
