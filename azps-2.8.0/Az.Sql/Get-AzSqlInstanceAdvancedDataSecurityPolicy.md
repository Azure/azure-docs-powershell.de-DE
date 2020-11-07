---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 847fc240d9ac30613c78d2d703aef76fcbc1661f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825556"
---
# <span data-ttu-id="4eb52-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="4eb52-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="4eb52-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4eb52-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb52-103">Ruft erweiterte Datensicherheitsrichtlinien einer verwalteten Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="4eb52-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="4eb52-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4eb52-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4eb52-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4eb52-105">DESCRIPTION</span></span>
<span data-ttu-id="4eb52-106">Das Cmdlet " **Get-AzSqlInstanceAdvancedDataSecurityPolicy** " Ruft die erweiterte Datensicherheitsrichtlinie einer verwalteten Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="4eb52-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="4eb52-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4eb52-107">EXAMPLES</span></span>

### <span data-ttu-id="4eb52-108">Beispiel 1 – ruft die erweiterte Datensicherheit für verwaltete Instanzen ab</span><span class="sxs-lookup"><span data-stu-id="4eb52-108">Example 1 - Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="4eb52-109">Beispiel 2 – Ruft die erweiterte Datensicherheit verwalteter Instanzen von der Ressource für verwaltete Instanzen ab</span><span class="sxs-lookup"><span data-stu-id="4eb52-109">Example 2 - Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="4eb52-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4eb52-110">PARAMETERS</span></span>

### <span data-ttu-id="4eb52-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb52-111">-DefaultProfile</span></span>
<span data-ttu-id="4eb52-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4eb52-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4eb52-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4eb52-113">-InputObject</span></span>
<span data-ttu-id="4eb52-114">Das mit der erweiterten Datensicherheitsrichtlinien Operation zu verwendende verwaltete Instanzen Objekt</span><span class="sxs-lookup"><span data-stu-id="4eb52-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="4eb52-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="4eb52-115">-InstanceName</span></span>
<span data-ttu-id="4eb52-116">Name der verwalteten Instanz der SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="4eb52-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="4eb52-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eb52-117">-ResourceGroupName</span></span>
<span data-ttu-id="4eb52-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4eb52-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="4eb52-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb52-119">CommonParameters</span></span>
<span data-ttu-id="4eb52-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eb52-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb52-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eb52-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb52-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4eb52-122">INPUTS</span></span>

### <span data-ttu-id="4eb52-123">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="4eb52-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="4eb52-124">System. String</span><span class="sxs-lookup"><span data-stu-id="4eb52-124">System.String</span></span>

## <span data-ttu-id="4eb52-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4eb52-125">OUTPUTS</span></span>

### <span data-ttu-id="4eb52-126">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="4eb52-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="4eb52-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="4eb52-127">NOTES</span></span>

## <span data-ttu-id="4eb52-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4eb52-128">RELATED LINKS</span></span>
