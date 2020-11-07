---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: a5aa9029e9d787311bb5b0c13b761c14f2b8bbca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824631"
---
# <span data-ttu-id="1bfdd-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="1bfdd-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="1bfdd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1bfdd-102">SYNOPSIS</span></span>
<span data-ttu-id="1bfdd-103">Deaktiviert die erweiterte Datensicherheit für eine verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="1bfdd-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="1bfdd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfdd-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1bfdd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1bfdd-105">DESCRIPTION</span></span>
<span data-ttu-id="1bfdd-106">Das Cmdlet **Disable-AzSqlInstanceAdvancedDataSecurity** deaktiviert die erweiterte Datensicherheit für eine verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="1bfdd-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="1bfdd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1bfdd-107">EXAMPLES</span></span>

### <span data-ttu-id="1bfdd-108">Beispiel 1: erweiterte Datensicherheit für verwaltete Instanzen deaktivieren</span><span class="sxs-lookup"><span data-stu-id="1bfdd-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="1bfdd-109">Beispiel 2 – Deaktivieren der erweiterten Datensicherheit für Server aus verwalteter Instanzen Ressource</span><span class="sxs-lookup"><span data-stu-id="1bfdd-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="1bfdd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bfdd-110">PARAMETERS</span></span>

### <span data-ttu-id="1bfdd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bfdd-111">-DefaultProfile</span></span>
<span data-ttu-id="1bfdd-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1bfdd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bfdd-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1bfdd-113">-InputObject</span></span>
<span data-ttu-id="1bfdd-114">Das mit der erweiterten Datensicherheitsrichtlinien Operation zu verwendende verwaltete Instanzen Objekt</span><span class="sxs-lookup"><span data-stu-id="1bfdd-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="1bfdd-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="1bfdd-115">-InstanceName</span></span>
<span data-ttu-id="1bfdd-116">Name der verwalteten Instanz der SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="1bfdd-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="1bfdd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bfdd-117">-ResourceGroupName</span></span>
<span data-ttu-id="1bfdd-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1bfdd-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="1bfdd-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1bfdd-119">-Confirm</span></span>
<span data-ttu-id="1bfdd-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1bfdd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bfdd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bfdd-121">-WhatIf</span></span>
<span data-ttu-id="1bfdd-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1bfdd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bfdd-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1bfdd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bfdd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bfdd-124">CommonParameters</span></span>
<span data-ttu-id="1bfdd-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bfdd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bfdd-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bfdd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bfdd-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1bfdd-127">INPUTS</span></span>

### <span data-ttu-id="1bfdd-128">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="1bfdd-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="1bfdd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1bfdd-129">System.String</span></span>

## <span data-ttu-id="1bfdd-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1bfdd-130">OUTPUTS</span></span>

### <span data-ttu-id="1bfdd-131">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="1bfdd-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="1bfdd-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="1bfdd-132">NOTES</span></span>

## <span data-ttu-id="1bfdd-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1bfdd-133">RELATED LINKS</span></span>
