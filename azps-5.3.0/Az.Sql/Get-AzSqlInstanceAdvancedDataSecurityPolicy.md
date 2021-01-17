---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 8adb699375a1b53f20e6027f35772642c658928b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468500"
---
# <span data-ttu-id="0136c-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="0136c-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="0136c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0136c-102">SYNOPSIS</span></span>
<span data-ttu-id="0136c-103">Ruft die Advanced Data Security-Richtlinie einer verwalteten Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="0136c-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="0136c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0136c-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0136c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0136c-105">DESCRIPTION</span></span>
<span data-ttu-id="0136c-106">Das **Cmdlet "Get-AzSqlInstanceAdvancedDataSecurityPolicy"** ruft die Advanced Data Security-Richtlinie einer verwalteten Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="0136c-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="0136c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0136c-107">EXAMPLES</span></span>

### <span data-ttu-id="0136c-108">Beispiel 1: Verwaltete Instanz Advanced Data Security</span><span class="sxs-lookup"><span data-stu-id="0136c-108">Example 1: Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="0136c-109">Beispiel 2: Ruft die verwaltete Instanz Advanced Data Security aus einer verwalteten Instanzressource ab.</span><span class="sxs-lookup"><span data-stu-id="0136c-109">Example 2: Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="0136c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0136c-110">PARAMETERS</span></span>

### <span data-ttu-id="0136c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0136c-111">-DefaultProfile</span></span>
<span data-ttu-id="0136c-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0136c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0136c-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0136c-113">-InputObject</span></span>
<span data-ttu-id="0136c-114">Das verwaltete Instanzobjekt, das für den Richtlinienvorgang "Advanced Data Security" verwendet wird</span><span class="sxs-lookup"><span data-stu-id="0136c-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0136c-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0136c-115">-InstanceName</span></span>
<span data-ttu-id="0136c-116">SQL Datenbank verwalteten Instanznamen.</span><span class="sxs-lookup"><span data-stu-id="0136c-116">SQL Database managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0136c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0136c-117">-ResourceGroupName</span></span>
<span data-ttu-id="0136c-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0136c-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="0136c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0136c-119">CommonParameters</span></span>
<span data-ttu-id="0136c-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0136c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0136c-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0136c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0136c-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0136c-122">INPUTS</span></span>

### <span data-ttu-id="0136c-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="0136c-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="0136c-124">System.String</span><span class="sxs-lookup"><span data-stu-id="0136c-124">System.String</span></span>

## <span data-ttu-id="0136c-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0136c-125">OUTPUTS</span></span>

### <span data-ttu-id="0136c-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="0136c-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="0136c-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0136c-127">NOTES</span></span>

## <span data-ttu-id="0136c-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0136c-128">RELATED LINKS</span></span>
