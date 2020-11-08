---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 1e3fdb2eabd986907a4b702a62caa3a0d9c34e85
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180276"
---
# <span data-ttu-id="7450b-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="7450b-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="7450b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7450b-102">SYNOPSIS</span></span>
<span data-ttu-id="7450b-103">Methode zum Abrufen eines Projekts migrieren.</span><span class="sxs-lookup"><span data-stu-id="7450b-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="7450b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7450b-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7450b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7450b-105">DESCRIPTION</span></span>
<span data-ttu-id="7450b-106">Methode zum Abrufen eines Projekts migrieren.</span><span class="sxs-lookup"><span data-stu-id="7450b-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="7450b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7450b-107">EXAMPLES</span></span>

### <span data-ttu-id="7450b-108">Beispiel 1: Abrufen</span><span class="sxs-lookup"><span data-stu-id="7450b-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="7450b-109">Methode zum Abrufen eines Projekts migrieren.</span><span class="sxs-lookup"><span data-stu-id="7450b-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="7450b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7450b-110">PARAMETERS</span></span>

### <span data-ttu-id="7450b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7450b-111">-DefaultProfile</span></span>
<span data-ttu-id="7450b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7450b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7450b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7450b-113">-Name</span></span>
<span data-ttu-id="7450b-114">Name des Azure-Migrationsprojekts</span><span class="sxs-lookup"><span data-stu-id="7450b-114">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrateProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7450b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7450b-115">-ResourceGroupName</span></span>
<span data-ttu-id="7450b-116">Der Name der Azure-Ressourcengruppe, in der Project migriert wird.</span><span class="sxs-lookup"><span data-stu-id="7450b-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7450b-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="7450b-117">-SubscriptionId</span></span>
<span data-ttu-id="7450b-118">Azure-Abonnement-ID, in der das Projekt "migrieren" erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7450b-118">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7450b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7450b-119">CommonParameters</span></span>
<span data-ttu-id="7450b-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7450b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7450b-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7450b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7450b-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7450b-122">INPUTS</span></span>

## <span data-ttu-id="7450b-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7450b-123">OUTPUTS</span></span>

### <span data-ttu-id="7450b-124">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180901Preview. IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="7450b-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="7450b-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="7450b-125">NOTES</span></span>

<span data-ttu-id="7450b-126">Aliase</span><span class="sxs-lookup"><span data-stu-id="7450b-126">ALIASES</span></span>

## <span data-ttu-id="7450b-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7450b-127">RELATED LINKS</span></span>

