---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: ae92a4fa28f0715c7a2517f062113afb01a359cf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360687"
---
# <span data-ttu-id="2cd16-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="2cd16-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="2cd16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cd16-102">SYNOPSIS</span></span>
<span data-ttu-id="2cd16-103">Failover einer Azure SQL verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="2cd16-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="2cd16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2cd16-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2cd16-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2cd16-105">DESCRIPTION</span></span>
<span data-ttu-id="2cd16-106">Das **Cmdlet Invoke-AzSqlInstanceFailover** über ein Azure SQL Verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="2cd16-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="2cd16-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2cd16-107">EXAMPLES</span></span>

### <span data-ttu-id="2cd16-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2cd16-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="2cd16-109">Mit diesem Befehl wird ein Failover für die primäre Replikat der Instanz mit dem Namen "ManagedInstance01" ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2cd16-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="2cd16-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2cd16-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="2cd16-111">Mit diesem Befehl wird ein Failover des lesbaren sekundären Replikats der verwalteten Instanz "ManagedInstance01" ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2cd16-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="2cd16-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cd16-112">PARAMETERS</span></span>

### <span data-ttu-id="2cd16-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cd16-113">-AsJob</span></span>
<span data-ttu-id="2cd16-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2cd16-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2cd16-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cd16-115">-DefaultProfile</span></span>
<span data-ttu-id="2cd16-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2cd16-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cd16-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2cd16-117">-Force</span></span>
<span data-ttu-id="2cd16-118">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="2cd16-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="2cd16-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2cd16-119">-Name</span></span>
<span data-ttu-id="2cd16-120">Der Name der Azure SQL zu entfernende Instanz.</span><span class="sxs-lookup"><span data-stu-id="2cd16-120">The name of the Azure SQL instance to remove.</span></span>

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

### <span data-ttu-id="2cd16-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2cd16-121">-PassThru</span></span>
<span data-ttu-id="2cd16-122">Bei erfolgreicher Ausführung wird "true" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2cd16-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="2cd16-123">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="2cd16-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2cd16-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="2cd16-124">-ReadableSecondary</span></span>
<span data-ttu-id="2cd16-125">Failover der lesbaren sekundären Replikate anstelle der primären Standardreplikate</span><span class="sxs-lookup"><span data-stu-id="2cd16-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="2cd16-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cd16-126">-ResourceGroupName</span></span>
<span data-ttu-id="2cd16-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2cd16-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="2cd16-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cd16-128">-Confirm</span></span>
<span data-ttu-id="2cd16-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2cd16-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cd16-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2cd16-130">-WhatIf</span></span>
<span data-ttu-id="2cd16-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2cd16-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2cd16-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2cd16-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cd16-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cd16-133">CommonParameters</span></span>
<span data-ttu-id="2cd16-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cd16-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cd16-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2cd16-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cd16-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2cd16-136">INPUTS</span></span>

### <span data-ttu-id="2cd16-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2cd16-137">System.String</span></span>

## <span data-ttu-id="2cd16-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2cd16-138">OUTPUTS</span></span>

## <span data-ttu-id="2cd16-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2cd16-139">NOTES</span></span>

## <span data-ttu-id="2cd16-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2cd16-140">RELATED LINKS</span></span>
