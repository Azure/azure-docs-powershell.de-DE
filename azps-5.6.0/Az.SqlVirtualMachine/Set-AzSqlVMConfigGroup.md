---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: 4dd2042ae3c7e84b9a7a82dde19fb5848229f51c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926248"
---
# <span data-ttu-id="bb3e6-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="bb3e6-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="bb3e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb3e6-102">SYNOPSIS</span></span>
<span data-ttu-id="bb3e6-103">Legen Sie die Informationen relativ zu einer Sql Virtual Machine-Gruppe in einer Sql Virtual Machine-Konfiguration ein.</span><span class="sxs-lookup"><span data-stu-id="bb3e6-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="bb3e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb3e6-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb3e6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb3e6-105">DESCRIPTION</span></span>
<span data-ttu-id="bb3e6-106">Im Set-AzSqlVMConfigGroup cmdlet werden die informationen festgelegt, die erforderlich sind, um einer Sql Virtual Machine-Gruppe für eine Sql Virtual Machine-Konfiguration bei beitritt.</span><span class="sxs-lookup"><span data-stu-id="bb3e6-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="bb3e6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bb3e6-107">EXAMPLES</span></span>

### <span data-ttu-id="bb3e6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bb3e6-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="bb3e6-109">Aktualisieren Sie die Gruppeninformationen einer Sql Virtual Machine-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="bb3e6-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="bb3e6-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bb3e6-110">PARAMETERS</span></span>

### <span data-ttu-id="bb3e6-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="bb3e6-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="bb3e6-112">Kennwort für das Cluster-Bootstrap-Konto</span><span class="sxs-lookup"><span data-stu-id="bb3e6-112">Password for the cluster bootstrap account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb3e6-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="bb3e6-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="bb3e6-114">Kennwort für das Konto des Clusteroperators</span><span class="sxs-lookup"><span data-stu-id="bb3e6-114">Password for the cluster operator account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb3e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb3e6-115">-DefaultProfile</span></span>
<span data-ttu-id="bb3e6-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb3e6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb3e6-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="bb3e6-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="bb3e6-118">Kennwort für das SQL Dienstkonto</span><span class="sxs-lookup"><span data-stu-id="bb3e6-118">Password for the SQL service account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb3e6-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="bb3e6-119">-SqlVM</span></span>
<span data-ttu-id="bb3e6-120">Die SQL konfiguration des virtuellen Computers, der die Gruppenmitgliedschaft hinzugefügt wird</span><span class="sxs-lookup"><span data-stu-id="bb3e6-120">The SQL virtual machine configuration which group membership will be added to</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb3e6-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="bb3e6-121">-SqlVMGroup</span></span>
<span data-ttu-id="bb3e6-122">Die Gruppe, SQL virtueller Computer Teil des</span><span class="sxs-lookup"><span data-stu-id="bb3e6-122">The group the SQL virtual machine will be part of</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb3e6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb3e6-123">CommonParameters</span></span>
<span data-ttu-id="bb3e6-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb3e6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb3e6-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb3e6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb3e6-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bb3e6-126">INPUTS</span></span>

### <span data-ttu-id="bb3e6-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="bb3e6-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="bb3e6-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bb3e6-128">OUTPUTS</span></span>

### <span data-ttu-id="bb3e6-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="bb3e6-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="bb3e6-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bb3e6-130">NOTES</span></span>

## <span data-ttu-id="bb3e6-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bb3e6-131">RELATED LINKS</span></span>
