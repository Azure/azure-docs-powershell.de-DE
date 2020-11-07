---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: b83dc58161791009a3adfd7cbf9b0b07b3f0b5b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846391"
---
# <span data-ttu-id="830f5-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="830f5-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="830f5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="830f5-102">SYNOPSIS</span></span>
<span data-ttu-id="830f5-103">Sie können die Informationen relativ zu einer virtuellen SQL-Computergruppe in einer virtuellen SQL-Computerkonfiguration einrichten.</span><span class="sxs-lookup"><span data-stu-id="830f5-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="830f5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="830f5-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="830f5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="830f5-105">DESCRIPTION</span></span>
<span data-ttu-id="830f5-106">Das Set-AzSqlVMConfigGroup-Cmdlet legt die erforderlichen Informationen für den Beitritt zu einer virtuellen SQL-Computergruppe für eine SQL-Konfiguration für virtuelle Maschinen an.</span><span class="sxs-lookup"><span data-stu-id="830f5-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="830f5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="830f5-107">EXAMPLES</span></span>

### <span data-ttu-id="830f5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="830f5-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="830f5-109">Aktualisieren Sie die Gruppeninformationen einer SQL Virtual Machine-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="830f5-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="830f5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="830f5-110">PARAMETERS</span></span>

### <span data-ttu-id="830f5-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="830f5-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="830f5-112">Kennwort für das Cluster-Bootstrap-Konto</span><span class="sxs-lookup"><span data-stu-id="830f5-112">Password for the cluster bootstrap account</span></span>

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

### <span data-ttu-id="830f5-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="830f5-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="830f5-114">Kennwort für das Cluster Operator Konto</span><span class="sxs-lookup"><span data-stu-id="830f5-114">Password for the cluster operator account</span></span>

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

### <span data-ttu-id="830f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="830f5-115">-DefaultProfile</span></span>
<span data-ttu-id="830f5-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="830f5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="830f5-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="830f5-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="830f5-118">Kennwort für das SQL-Dienstkonto</span><span class="sxs-lookup"><span data-stu-id="830f5-118">Password for the SQL service account</span></span>

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

### <span data-ttu-id="830f5-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="830f5-119">-SqlVM</span></span>
<span data-ttu-id="830f5-120">Die Konfiguration des SQL-virtuellen Computers, zu der die Gruppenmitgliedschaft hinzugefügt wird</span><span class="sxs-lookup"><span data-stu-id="830f5-120">The SQL virtual machine configuration which group membership will be added to</span></span>

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

### <span data-ttu-id="830f5-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="830f5-121">-SqlVMGroup</span></span>
<span data-ttu-id="830f5-122">Die Gruppe, in der sich der virtuelle SQL-Computer befindet</span><span class="sxs-lookup"><span data-stu-id="830f5-122">The group the SQL virtual machine will be part of</span></span>

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

### <span data-ttu-id="830f5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="830f5-123">CommonParameters</span></span>
<span data-ttu-id="830f5-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="830f5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="830f5-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="830f5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="830f5-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="830f5-126">INPUTS</span></span>

### <span data-ttu-id="830f5-127">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="830f5-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="830f5-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="830f5-128">OUTPUTS</span></span>

### <span data-ttu-id="830f5-129">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="830f5-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="830f5-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="830f5-130">NOTES</span></span>

## <span data-ttu-id="830f5-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="830f5-131">RELATED LINKS</span></span>
