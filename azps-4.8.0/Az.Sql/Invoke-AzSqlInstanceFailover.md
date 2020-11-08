---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: ae92a4fa28f0715c7a2517f062113afb01a359cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166052"
---
# <span data-ttu-id="6c573-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="6c573-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="6c573-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c573-102">SYNOPSIS</span></span>
<span data-ttu-id="6c573-103">Failover einer Azure SQL-verwalteten Instanz.</span><span class="sxs-lookup"><span data-stu-id="6c573-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="6c573-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c573-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c573-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c573-105">DESCRIPTION</span></span>
<span data-ttu-id="6c573-106">Das Cmdlet **Invoke-AzSqlInstanceFailover** Failover eine Azure SQL-verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="6c573-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="6c573-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c573-107">EXAMPLES</span></span>

### <span data-ttu-id="6c573-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6c573-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="6c573-109">Mit diesem Befehl wird das primäre Replikat der Instanz mit dem Namen "ManagedInstance01" Failover.</span><span class="sxs-lookup"><span data-stu-id="6c573-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="6c573-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6c573-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="6c573-111">Mit diesem Befehl wird das lesbare sekundäre Replikat der verwalteten Instanz "ManagedInstance01" Failover.</span><span class="sxs-lookup"><span data-stu-id="6c573-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="6c573-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c573-112">PARAMETERS</span></span>

### <span data-ttu-id="6c573-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c573-113">-AsJob</span></span>
<span data-ttu-id="6c573-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6c573-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c573-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c573-115">-DefaultProfile</span></span>
<span data-ttu-id="6c573-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6c573-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c573-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6c573-117">-Force</span></span>
<span data-ttu-id="6c573-118">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="6c573-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="6c573-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6c573-119">-Name</span></span>
<span data-ttu-id="6c573-120">Der Name der zu entfernenden Azure SQL-Instanz.</span><span class="sxs-lookup"><span data-stu-id="6c573-120">The name of the Azure SQL instance to remove.</span></span>

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

### <span data-ttu-id="6c573-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c573-121">-PassThru</span></span>
<span data-ttu-id="6c573-122">Gibt bei erfolgreicher Ausführung true zurück.</span><span class="sxs-lookup"><span data-stu-id="6c573-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="6c573-123">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="6c573-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6c573-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="6c573-124">-ReadableSecondary</span></span>
<span data-ttu-id="6c573-125">Failover des lesbaren sekundären Replikats anstelle des standardmäßigen primären Replikats</span><span class="sxs-lookup"><span data-stu-id="6c573-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="6c573-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c573-126">-ResourceGroupName</span></span>
<span data-ttu-id="6c573-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6c573-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="6c573-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6c573-128">-Confirm</span></span>
<span data-ttu-id="6c573-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6c573-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c573-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c573-130">-WhatIf</span></span>
<span data-ttu-id="6c573-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6c573-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c573-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c573-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c573-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c573-133">CommonParameters</span></span>
<span data-ttu-id="6c573-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c573-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c573-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c573-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c573-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c573-136">INPUTS</span></span>

### <span data-ttu-id="6c573-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6c573-137">System.String</span></span>

## <span data-ttu-id="6c573-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c573-138">OUTPUTS</span></span>

## <span data-ttu-id="6c573-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c573-139">NOTES</span></span>

## <span data-ttu-id="6c573-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c573-140">RELATED LINKS</span></span>
