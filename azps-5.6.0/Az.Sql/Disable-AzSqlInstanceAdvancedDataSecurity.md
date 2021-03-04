---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 4116ddf22bb39ddfa78e07180aaf61da7e87bb7f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933688"
---
# <span data-ttu-id="87961-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="87961-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="87961-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87961-102">SYNOPSIS</span></span>
<span data-ttu-id="87961-103">Deaktiviert Advanced Data Security für eine verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="87961-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="87961-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87961-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87961-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87961-105">DESCRIPTION</span></span>
<span data-ttu-id="87961-106">Das **Cmdlet Disable-AzSqlInstanceAdvancedDataSecurity** deaktiviert Advanced Data Security für eine verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="87961-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="87961-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="87961-107">EXAMPLES</span></span>

### <span data-ttu-id="87961-108">Beispiel 1 : Deaktivieren der verwalteten Instanz Advanced Data Security</span><span class="sxs-lookup"><span data-stu-id="87961-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="87961-109">Beispiel 2: Deaktivieren der erweiterten Serverdatensicherheit von einer verwalteten Instanzressource</span><span class="sxs-lookup"><span data-stu-id="87961-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="87961-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="87961-110">PARAMETERS</span></span>

### <span data-ttu-id="87961-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87961-111">-DefaultProfile</span></span>
<span data-ttu-id="87961-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87961-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87961-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87961-113">-InputObject</span></span>
<span data-ttu-id="87961-114">Das verwaltete Instanzobjekt, das mit dem Richtlinienvorgang "Advanced Data Security" verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="87961-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="87961-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="87961-115">-InstanceName</span></span>
<span data-ttu-id="87961-116">SQL Name der verwalteten Datenbank.</span><span class="sxs-lookup"><span data-stu-id="87961-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="87961-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87961-117">-ResourceGroupName</span></span>
<span data-ttu-id="87961-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="87961-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="87961-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="87961-119">-Confirm</span></span>
<span data-ttu-id="87961-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87961-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87961-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87961-121">-WhatIf</span></span>
<span data-ttu-id="87961-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87961-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87961-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87961-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87961-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87961-124">CommonParameters</span></span>
<span data-ttu-id="87961-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87961-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87961-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87961-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87961-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="87961-127">INPUTS</span></span>

### <span data-ttu-id="87961-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="87961-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="87961-129">System.String</span><span class="sxs-lookup"><span data-stu-id="87961-129">System.String</span></span>

## <span data-ttu-id="87961-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="87961-130">OUTPUTS</span></span>

### <span data-ttu-id="87961-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="87961-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="87961-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="87961-132">NOTES</span></span>

## <span data-ttu-id="87961-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="87961-133">RELATED LINKS</span></span>
