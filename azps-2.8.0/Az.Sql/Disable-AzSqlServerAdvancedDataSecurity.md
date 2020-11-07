---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: ca3b39ac369900f19c41b27b50efb06af7cf2056
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825319"
---
# <span data-ttu-id="557c5-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="557c5-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="557c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="557c5-102">SYNOPSIS</span></span>
<span data-ttu-id="557c5-103">Deaktiviert die erweiterte Datensicherheit auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="557c5-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="557c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="557c5-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="557c5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="557c5-105">DESCRIPTION</span></span>
<span data-ttu-id="557c5-106">Das Cmdlet **Disable-AzSqlServerAdvancedDataSecurity** deaktiviert die erweiterte Datensicherheit auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="557c5-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="557c5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="557c5-107">EXAMPLES</span></span>

### <span data-ttu-id="557c5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="557c5-108">Example 1</span></span>
### <span data-ttu-id="557c5-109">Beispiel 1 – Deaktivieren der erweiterten Datensicherheit für den Server</span><span class="sxs-lookup"><span data-stu-id="557c5-109">Example 1 - Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="557c5-110">Beispiel 2: Deaktivieren der erweiterten Datensicherheit des Servers von der Server Ressource</span><span class="sxs-lookup"><span data-stu-id="557c5-110">Example 2 - Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="557c5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="557c5-111">PARAMETERS</span></span>

### <span data-ttu-id="557c5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="557c5-112">-DefaultProfile</span></span>
<span data-ttu-id="557c5-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="557c5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="557c5-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="557c5-114">-InputObject</span></span>
<span data-ttu-id="557c5-115">Das Serverobjekt, das mit der erweiterten Datensicherheitsrichtlinien Operation verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="557c5-115">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="557c5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="557c5-116">-ResourceGroupName</span></span>
<span data-ttu-id="557c5-117">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="557c5-117">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="557c5-118">-Servername</span><span class="sxs-lookup"><span data-stu-id="557c5-118">-ServerName</span></span>
<span data-ttu-id="557c5-119">SQL-Datenbankservername</span><span class="sxs-lookup"><span data-stu-id="557c5-119">SQL Database server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="557c5-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="557c5-120">-Confirm</span></span>
<span data-ttu-id="557c5-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="557c5-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="557c5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="557c5-122">-WhatIf</span></span>
<span data-ttu-id="557c5-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="557c5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="557c5-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="557c5-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="557c5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="557c5-125">CommonParameters</span></span>
<span data-ttu-id="557c5-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="557c5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="557c5-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="557c5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="557c5-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="557c5-128">INPUTS</span></span>

### <span data-ttu-id="557c5-129">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="557c5-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="557c5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="557c5-130">System.String</span></span>

## <span data-ttu-id="557c5-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="557c5-131">OUTPUTS</span></span>

### <span data-ttu-id="557c5-132">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="557c5-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="557c5-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="557c5-133">NOTES</span></span>

## <span data-ttu-id="557c5-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="557c5-134">RELATED LINKS</span></span>
