---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: cde8f48ebef73e3669a82f05c2ba91a4a4e4c582
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929360"
---
# <span data-ttu-id="50d8b-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="50d8b-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="50d8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="50d8b-103">Failover einer Azure SQL verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="50d8b-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="50d8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50d8b-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50d8b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50d8b-105">DESCRIPTION</span></span>
<span data-ttu-id="50d8b-106">Das **Cmdlet Invoke-AzSqlInstanceFailover** failovert eine Azure SQL verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="50d8b-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="50d8b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="50d8b-107">EXAMPLES</span></span>

### <span data-ttu-id="50d8b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="50d8b-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="50d8b-109">Dieser Befehl über failovert das primäre Replikat der Instanz mit dem Namen "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="50d8b-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="50d8b-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="50d8b-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="50d8b-111">Mit diesem Befehl wird das lesbare sekundäre Replikat der verwalteten Instanz "ManagedInstance01" failovern.</span><span class="sxs-lookup"><span data-stu-id="50d8b-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="50d8b-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="50d8b-112">PARAMETERS</span></span>

### <span data-ttu-id="50d8b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50d8b-113">-AsJob</span></span>
<span data-ttu-id="50d8b-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="50d8b-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d8b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50d8b-115">-DefaultProfile</span></span>
<span data-ttu-id="50d8b-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50d8b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50d8b-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="50d8b-117">-Force</span></span>
<span data-ttu-id="50d8b-118">Bestätigungsmeldung überspringen zum Ausführen der Aktion</span><span class="sxs-lookup"><span data-stu-id="50d8b-118">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d8b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="50d8b-119">-Name</span></span>
<span data-ttu-id="50d8b-120">Der Name der azure SQL zu entfernende Instanz.</span><span class="sxs-lookup"><span data-stu-id="50d8b-120">The name of the Azure SQL instance to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50d8b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50d8b-121">-PassThru</span></span>
<span data-ttu-id="50d8b-122">Gibt bei erfolgreicher Ausführung den Wert "true" zurück.</span><span class="sxs-lookup"><span data-stu-id="50d8b-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="50d8b-123">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="50d8b-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d8b-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="50d8b-124">-ReadableSecondary</span></span>
<span data-ttu-id="50d8b-125">Failover des lesbaren sekundären Replikats anstelle des primären Standardreplikates</span><span class="sxs-lookup"><span data-stu-id="50d8b-125">Failover the readable secondary replica instead of the default primary replica</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d8b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50d8b-126">-ResourceGroupName</span></span>
<span data-ttu-id="50d8b-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="50d8b-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="50d8b-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="50d8b-128">-Confirm</span></span>
<span data-ttu-id="50d8b-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="50d8b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50d8b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50d8b-130">-WhatIf</span></span>
<span data-ttu-id="50d8b-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50d8b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50d8b-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="50d8b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50d8b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50d8b-133">CommonParameters</span></span>
<span data-ttu-id="50d8b-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50d8b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50d8b-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50d8b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50d8b-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="50d8b-136">INPUTS</span></span>

### <span data-ttu-id="50d8b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="50d8b-137">System.String</span></span>

## <span data-ttu-id="50d8b-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="50d8b-138">OUTPUTS</span></span>

## <span data-ttu-id="50d8b-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="50d8b-139">NOTES</span></span>

## <span data-ttu-id="50d8b-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="50d8b-140">RELATED LINKS</span></span>
