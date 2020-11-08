---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: 5282b3d0ae145088cf07040520050937f8d3a335
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177542"
---
# <span data-ttu-id="7e30c-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="7e30c-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="7e30c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e30c-102">SYNOPSIS</span></span>
<span data-ttu-id="7e30c-103">Ruft eine bestimmte Registrierungs Definition oder eine Liste der Registrierungs Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="7e30c-103">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="7e30c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e30c-104">SYNTAX</span></span>

### <span data-ttu-id="7e30c-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7e30c-105">ByName (Default)</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e30c-106">Standard</span><span class="sxs-lookup"><span data-stu-id="7e30c-106">Default</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e30c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e30c-107">DESCRIPTION</span></span>
<span data-ttu-id="7e30c-108">Ruft eine bestimmte Registrierungs Definition oder eine Liste der Registrierungs Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="7e30c-108">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="7e30c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e30c-109">EXAMPLES</span></span>

### <span data-ttu-id="7e30c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7e30c-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesDefinition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="7e30c-111">Ruft alle Registrierungs Definitionen im Standardbereich ab.</span><span class="sxs-lookup"><span data-stu-id="7e30c-111">Gets all registration definitions at default scope.</span></span>

### <span data-ttu-id="7e30c-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7e30c-112">Example 2</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="7e30c-113">Ruft die Registrierungs Definition nach Name im Standardbereich ab.</span><span class="sxs-lookup"><span data-stu-id="7e30c-113">Gets the registration definition by name at default scope.</span></span>

### <span data-ttu-id="7e30c-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="7e30c-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="7e30c-115">Ruft alle Registrierungs Definitionen im angegebenen Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="7e30c-115">Gets all registration definitions at the given scope.</span></span>

## <span data-ttu-id="7e30c-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e30c-116">PARAMETERS</span></span>

### <span data-ttu-id="7e30c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e30c-117">-DefaultProfile</span></span>
<span data-ttu-id="7e30c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7e30c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e30c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7e30c-119">-Name</span></span>
<span data-ttu-id="7e30c-120">Der eindeutige Name der Registrierungs Definition.</span><span class="sxs-lookup"><span data-stu-id="7e30c-120">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="7e30c-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="7e30c-121">-Scope</span></span>
<span data-ttu-id="7e30c-122">Der Bereich, in dem die Registrierungs Definition erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7e30c-122">The scope where the registration definition created.</span></span>

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

### <span data-ttu-id="7e30c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e30c-123">CommonParameters</span></span>
<span data-ttu-id="7e30c-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e30c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e30c-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e30c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e30c-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e30c-126">INPUTS</span></span>

### <span data-ttu-id="7e30c-127">Keine</span><span class="sxs-lookup"><span data-stu-id="7e30c-127">None</span></span>
## <span data-ttu-id="7e30c-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e30c-128">OUTPUTS</span></span>

### <span data-ttu-id="7e30c-129">Microsoft. Azure. PowerShell. Cmdlets. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="7e30c-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="7e30c-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e30c-130">NOTES</span></span>

## <span data-ttu-id="7e30c-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e30c-131">RELATED LINKS</span></span>
