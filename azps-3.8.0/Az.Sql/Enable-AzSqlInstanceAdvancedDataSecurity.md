---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 981baf0b0cd4d3ca70d18ab43b08bb2a16f7708f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846775"
---
# <span data-ttu-id="9303e-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="9303e-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="9303e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9303e-102">SYNOPSIS</span></span>
<span data-ttu-id="9303e-103">Ermöglicht erweiterte Datensicherheit für eine verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="9303e-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="9303e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9303e-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9303e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9303e-105">DESCRIPTION</span></span>
<span data-ttu-id="9303e-106">Das Cmdlet **enable-AzSqlInstanceAdvancedDataSecurity** ermöglicht erweiterte Datensicherheit für eine verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="9303e-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span> <span data-ttu-id="9303e-107">Advanced Data Security ist ein einheitliches Sicherheitspaket, das die Datenklassifizierung, die Anfälligkeitsbewertung und den erweiterten Bedrohungsschutz für Ihre verwaltete Instanz umfasst.</span><span class="sxs-lookup"><span data-stu-id="9303e-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your managed instance.</span></span> <span data-ttu-id="9303e-108">(Es wird automatisch ein neues Speicherkonto zum Speichern von Sicherheitsrisikobewertungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="9303e-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="9303e-109">Wenn zuvor ein Speicherkonto für diesen Zweck erstellt wurde, wird es stattdessen verwendet.</span><span class="sxs-lookup"><span data-stu-id="9303e-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="9303e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9303e-110">EXAMPLES</span></span>

### <span data-ttu-id="9303e-111">Beispiel 1 – erweiterte Datensicherheit für verwaltete Instanzen aktivieren</span><span class="sxs-lookup"><span data-stu-id="9303e-111">Example 1 - Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="9303e-112">Beispiel 2 – erweiterte Datensicherheit für verwaltete Instanzen von Serverressourcen aktivieren</span><span class="sxs-lookup"><span data-stu-id="9303e-112">Example 2 - Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="9303e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9303e-113">PARAMETERS</span></span>

### <span data-ttu-id="9303e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9303e-114">-AsJob</span></span>
<span data-ttu-id="9303e-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9303e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9303e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9303e-116">-DefaultProfile</span></span>
<span data-ttu-id="9303e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9303e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9303e-118">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="9303e-118">-DeploymentName</span></span>
<span data-ttu-id="9303e-119">Angeben eines benutzerdefinierten Namens für die erweiterte Bereitstellung von Datensicherheit</span><span class="sxs-lookup"><span data-stu-id="9303e-119">Supply a custom name for Advanced Data Security deployment</span></span>

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

### <span data-ttu-id="9303e-120">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="9303e-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="9303e-121">Sicherheitsrisikobewertung nicht automatisch aktivieren (Dadurch wird kein Speicherkonto erstellt)</span><span class="sxs-lookup"><span data-stu-id="9303e-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="9303e-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9303e-122">-InputObject</span></span>
<span data-ttu-id="9303e-123">Das mit der erweiterten Datensicherheitsrichtlinien Operation zu verwendende verwaltete Instanzen Objekt</span><span class="sxs-lookup"><span data-stu-id="9303e-123">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="9303e-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9303e-124">-InstanceName</span></span>
<span data-ttu-id="9303e-125">Name der verwalteten Instanz der SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="9303e-125">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="9303e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9303e-126">-ResourceGroupName</span></span>
<span data-ttu-id="9303e-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9303e-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="9303e-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9303e-128">-Confirm</span></span>
<span data-ttu-id="9303e-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9303e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9303e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9303e-130">-WhatIf</span></span>
<span data-ttu-id="9303e-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9303e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9303e-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9303e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9303e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9303e-133">CommonParameters</span></span>
<span data-ttu-id="9303e-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9303e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9303e-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9303e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9303e-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9303e-136">INPUTS</span></span>

### <span data-ttu-id="9303e-137">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="9303e-137">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="9303e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9303e-138">System.String</span></span>

## <span data-ttu-id="9303e-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9303e-139">OUTPUTS</span></span>

### <span data-ttu-id="9303e-140">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="9303e-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="9303e-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="9303e-141">NOTES</span></span>

## <span data-ttu-id="9303e-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9303e-142">RELATED LINKS</span></span>
