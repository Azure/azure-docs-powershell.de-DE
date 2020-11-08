---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: c9427df1710ad7232cf66ce576cf2c3db409f7d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004496"
---
# <span data-ttu-id="26dcf-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="26dcf-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="26dcf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26dcf-102">SYNOPSIS</span></span>
<span data-ttu-id="26dcf-103">Ruft erweiterte Datensicherheitsrichtlinien einer verwalteten Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="26dcf-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="26dcf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="26dcf-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26dcf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26dcf-105">DESCRIPTION</span></span>
<span data-ttu-id="26dcf-106">Das Cmdlet " **Get-AzSqlInstanceAdvancedDataSecurityPolicy** " Ruft die erweiterte Datensicherheitsrichtlinie einer verwalteten Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="26dcf-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="26dcf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26dcf-107">EXAMPLES</span></span>

### <span data-ttu-id="26dcf-108">Beispiel 1 – ruft die erweiterte Datensicherheit für verwaltete Instanzen ab</span><span class="sxs-lookup"><span data-stu-id="26dcf-108">Example 1 - Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="26dcf-109">Beispiel 2 – Ruft die erweiterte Datensicherheit verwalteter Instanzen von der Ressource für verwaltete Instanzen ab</span><span class="sxs-lookup"><span data-stu-id="26dcf-109">Example 2 - Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="26dcf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="26dcf-110">PARAMETERS</span></span>

### <span data-ttu-id="26dcf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26dcf-111">-DefaultProfile</span></span>
<span data-ttu-id="26dcf-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="26dcf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26dcf-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="26dcf-113">-InputObject</span></span>
<span data-ttu-id="26dcf-114">Das mit der erweiterten Datensicherheitsrichtlinien Operation zu verwendende verwaltete Instanzen Objekt</span><span class="sxs-lookup"><span data-stu-id="26dcf-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="26dcf-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="26dcf-115">-InstanceName</span></span>
<span data-ttu-id="26dcf-116">Name der verwalteten Instanz der SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="26dcf-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="26dcf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26dcf-117">-ResourceGroupName</span></span>
<span data-ttu-id="26dcf-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="26dcf-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="26dcf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26dcf-119">CommonParameters</span></span>
<span data-ttu-id="26dcf-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26dcf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26dcf-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26dcf-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26dcf-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26dcf-122">INPUTS</span></span>

### <span data-ttu-id="26dcf-123">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="26dcf-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="26dcf-124">System. String</span><span class="sxs-lookup"><span data-stu-id="26dcf-124">System.String</span></span>

## <span data-ttu-id="26dcf-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26dcf-125">OUTPUTS</span></span>

### <span data-ttu-id="26dcf-126">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="26dcf-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="26dcf-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="26dcf-127">NOTES</span></span>

## <span data-ttu-id="26dcf-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26dcf-128">RELATED LINKS</span></span>
