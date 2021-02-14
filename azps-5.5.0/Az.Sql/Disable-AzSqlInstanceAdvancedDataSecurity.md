---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 39b23c1b39121f143791667ade542080ba70ec95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163433"
---
# <span data-ttu-id="84d69-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="84d69-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="84d69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84d69-102">SYNOPSIS</span></span>
<span data-ttu-id="84d69-103">Deaktiviert Advanced Data Security für eine verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="84d69-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="84d69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84d69-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84d69-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84d69-105">DESCRIPTION</span></span>
<span data-ttu-id="84d69-106">Das **Cmdlet Disable-AzSqlInstanceAdvancedDataSecurity** deaktiviert Advanced Data Security für eine verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="84d69-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="84d69-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="84d69-107">EXAMPLES</span></span>

### <span data-ttu-id="84d69-108">Beispiel 1: Deaktivieren der verwalteten Instanz Advanced Data Security</span><span class="sxs-lookup"><span data-stu-id="84d69-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="84d69-109">Beispiel 2: Deaktivieren der erweiterten Datensicherheit des Servers aus einer verwalteten Instanzressource</span><span class="sxs-lookup"><span data-stu-id="84d69-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="84d69-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84d69-110">PARAMETERS</span></span>

### <span data-ttu-id="84d69-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84d69-111">-DefaultProfile</span></span>
<span data-ttu-id="84d69-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="84d69-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84d69-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84d69-113">-InputObject</span></span>
<span data-ttu-id="84d69-114">Das verwaltete Instanzobjekt, das für den Richtlinienvorgang "Advanced Data Security" verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="84d69-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="84d69-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="84d69-115">-InstanceName</span></span>
<span data-ttu-id="84d69-116">SQL Datenbank verwalteten Instanznamen.</span><span class="sxs-lookup"><span data-stu-id="84d69-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="84d69-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84d69-117">-ResourceGroupName</span></span>
<span data-ttu-id="84d69-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="84d69-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="84d69-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84d69-119">-Confirm</span></span>
<span data-ttu-id="84d69-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="84d69-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84d69-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="84d69-121">-WhatIf</span></span>
<span data-ttu-id="84d69-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84d69-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84d69-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="84d69-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84d69-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84d69-124">CommonParameters</span></span>
<span data-ttu-id="84d69-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84d69-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84d69-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84d69-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84d69-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="84d69-127">INPUTS</span></span>

### <span data-ttu-id="84d69-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="84d69-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="84d69-129">System.String</span><span class="sxs-lookup"><span data-stu-id="84d69-129">System.String</span></span>

## <span data-ttu-id="84d69-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="84d69-130">OUTPUTS</span></span>

### <span data-ttu-id="84d69-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="84d69-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="84d69-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="84d69-132">NOTES</span></span>

## <span data-ttu-id="84d69-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="84d69-133">RELATED LINKS</span></span>
