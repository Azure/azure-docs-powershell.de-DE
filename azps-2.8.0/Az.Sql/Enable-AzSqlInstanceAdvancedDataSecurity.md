---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 278c80206e1221550afc5c603c618c8219ea152f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825316"
---
# <span data-ttu-id="a3664-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="a3664-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="a3664-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3664-102">SYNOPSIS</span></span>
<span data-ttu-id="a3664-103">Ermöglicht erweiterte Datensicherheit für eine verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="a3664-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="a3664-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3664-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3664-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3664-105">DESCRIPTION</span></span>
<span data-ttu-id="a3664-106">Das Cmdlet **enable-AzSqlInstanceAdvancedDataSecurity** ermöglicht erweiterte Datensicherheit für eine verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="a3664-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span> <span data-ttu-id="a3664-107">Advanced Data Security ist ein einheitliches Sicherheitspaket, das die Datenklassifizierung, die Anfälligkeitsbewertung und den erweiterten Bedrohungsschutz für Ihre verwaltete Instanz umfasst.</span><span class="sxs-lookup"><span data-stu-id="a3664-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your managed instance.</span></span> <span data-ttu-id="a3664-108">(Es wird automatisch ein neues Speicherkonto zum Speichern von Sicherheitsrisikobewertungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="a3664-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="a3664-109">Wenn zuvor ein Speicherkonto für diesen Zweck erstellt wurde, wird es stattdessen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3664-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="a3664-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3664-110">EXAMPLES</span></span>

### <span data-ttu-id="a3664-111">Beispiel 1 – erweiterte Datensicherheit für verwaltete Instanzen aktivieren</span><span class="sxs-lookup"><span data-stu-id="a3664-111">Example 1 - Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="a3664-112">Beispiel 2 – erweiterte Datensicherheit für verwaltete Instanzen von Serverressourcen aktivieren</span><span class="sxs-lookup"><span data-stu-id="a3664-112">Example 2 - Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="a3664-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3664-113">PARAMETERS</span></span>

### <span data-ttu-id="a3664-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3664-114">-AsJob</span></span>
<span data-ttu-id="a3664-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a3664-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3664-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3664-116">-DefaultProfile</span></span>
<span data-ttu-id="a3664-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3664-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3664-118">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="a3664-118">-DeploymentName</span></span>
<span data-ttu-id="a3664-119">Angeben eines benutzerdefinierten Namens für die erweiterte Bereitstellung von Datensicherheit</span><span class="sxs-lookup"><span data-stu-id="a3664-119">Supply a custom name for Advanced Data Security deployment</span></span>

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

### <span data-ttu-id="a3664-120">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="a3664-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="a3664-121">Sicherheitsrisikobewertung nicht automatisch aktivieren (Dadurch wird kein Speicherkonto erstellt)</span><span class="sxs-lookup"><span data-stu-id="a3664-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="a3664-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a3664-122">-InputObject</span></span>
<span data-ttu-id="a3664-123">Das mit der erweiterten Datensicherheitsrichtlinien Operation zu verwendende verwaltete Instanzen Objekt</span><span class="sxs-lookup"><span data-stu-id="a3664-123">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="a3664-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a3664-124">-InstanceName</span></span>
<span data-ttu-id="a3664-125">Name der verwalteten Instanz der SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="a3664-125">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="a3664-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3664-126">-ResourceGroupName</span></span>
<span data-ttu-id="a3664-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a3664-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="a3664-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a3664-128">-Confirm</span></span>
<span data-ttu-id="a3664-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3664-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3664-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3664-130">-WhatIf</span></span>
<span data-ttu-id="a3664-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3664-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3664-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3664-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3664-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3664-133">CommonParameters</span></span>
<span data-ttu-id="a3664-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3664-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3664-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3664-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3664-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3664-136">INPUTS</span></span>

### <span data-ttu-id="a3664-137">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="a3664-137">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="a3664-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a3664-138">System.String</span></span>

## <span data-ttu-id="a3664-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3664-139">OUTPUTS</span></span>

### <span data-ttu-id="a3664-140">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a3664-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="a3664-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3664-141">NOTES</span></span>

## <span data-ttu-id="a3664-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3664-142">RELATED LINKS</span></span>
