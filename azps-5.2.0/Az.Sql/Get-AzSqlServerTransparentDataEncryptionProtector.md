---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: a2920eb845a162ac83f41e5c8de8c47848485431
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301859"
---
# <span data-ttu-id="09f90-101">Get-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="09f90-101">Get-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="09f90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09f90-102">SYNOPSIS</span></span>
<span data-ttu-id="09f90-103">Ruft die transparente Datenverschlüsselung (Transparent Data Encryption, TDE) ab</span><span class="sxs-lookup"><span data-stu-id="09f90-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

## <span data-ttu-id="09f90-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09f90-104">SYNTAX</span></span>

```
Get-AzSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09f90-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09f90-105">DESCRIPTION</span></span>
<span data-ttu-id="09f90-106">Das Get-AzSqlServerTransparentDataEncryptionProtector cmdlet ruft Informationen über das TDE-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="09f90-106">The Get-AzSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="09f90-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="09f90-107">EXAMPLES</span></span>

### <span data-ttu-id="09f90-108">Beispiel 1: Verwenden der transparenten Datenverschlüsselung (TDE)</span><span class="sxs-lookup"><span data-stu-id="09f90-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="09f90-109">Dieser Befehl ruft das TDE-Element für den Server mit dem Namen "ContosoServer" in der Ressourcengruppe "ContosoResourceGroup" ab.</span><span class="sxs-lookup"><span data-stu-id="09f90-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="09f90-110">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="09f90-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="09f90-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="09f90-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="09f90-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09f90-112">PARAMETERS</span></span>

### <span data-ttu-id="09f90-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f90-113">-DefaultProfile</span></span>
<span data-ttu-id="09f90-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="09f90-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09f90-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09f90-115">-ResourceGroupName</span></span>
<span data-ttu-id="09f90-116">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="09f90-116">The name of the resource group</span></span>

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

### <span data-ttu-id="09f90-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="09f90-117">-ServerName</span></span>
<span data-ttu-id="09f90-118">Der Azure Sql Server-Name.</span><span class="sxs-lookup"><span data-stu-id="09f90-118">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09f90-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09f90-119">-Confirm</span></span>
<span data-ttu-id="09f90-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="09f90-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09f90-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="09f90-121">-WhatIf</span></span>
<span data-ttu-id="09f90-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09f90-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09f90-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09f90-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09f90-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f90-124">CommonParameters</span></span>
<span data-ttu-id="09f90-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09f90-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f90-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09f90-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f90-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="09f90-127">INPUTS</span></span>

### <span data-ttu-id="09f90-128">System.String</span><span class="sxs-lookup"><span data-stu-id="09f90-128">System.String</span></span>

## <span data-ttu-id="09f90-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="09f90-129">OUTPUTS</span></span>

### <span data-ttu-id="09f90-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="09f90-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="09f90-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="09f90-131">NOTES</span></span>

## <span data-ttu-id="09f90-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="09f90-132">RELATED LINKS</span></span>

[<span data-ttu-id="09f90-133">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="09f90-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
