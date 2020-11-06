---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: 174bccd7b682c1c4922a5ca7b6bbfbd406667df0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478906"
---
# <span data-ttu-id="75a89-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="75a89-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="75a89-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75a89-102">SYNOPSIS</span></span>
<span data-ttu-id="75a89-103">Ruft die transparente Datenverschlüsselung (DSA)-Beschützer ab</span><span class="sxs-lookup"><span data-stu-id="75a89-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75a89-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75a89-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75a89-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75a89-105">DESCRIPTION</span></span>
<span data-ttu-id="75a89-106">Das Get-AzureRmSqlServerTransparentDataEncryptionProtector-Cmdlet ruft Informationen zur DSA-Beschützer ab.</span><span class="sxs-lookup"><span data-stu-id="75a89-106">The Get-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="75a89-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75a89-107">EXAMPLES</span></span>

### <span data-ttu-id="75a89-108">--------------------------Beispiel 1: erhalten Sie die transparente Datenverschlüsselung (DSA) Protector--------------------------</span><span class="sxs-lookup"><span data-stu-id="75a89-108">--------------------------  Example 1: Get the Transparent Data Encryption (TDE) protector  --------------------------</span></span>
```
PS C:\> Get-AzureRmSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="75a89-109">Dieser Befehl ruft die DSA-Beschützer für den Server mit dem Namen ContosoServer in der Ressourcengruppe mit dem Namen ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="75a89-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>

<span data-ttu-id="75a89-110">ResourceGroupName Servername Typ ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="75a89-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="75a89-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="75a89-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="75a89-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="75a89-112">PARAMETERS</span></span>

### <span data-ttu-id="75a89-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75a89-113">-ResourceGroupName</span></span>
<span data-ttu-id="75a89-114">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="75a89-114">The name of the resource group</span></span>

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

### <span data-ttu-id="75a89-115">-Servername</span><span class="sxs-lookup"><span data-stu-id="75a89-115">-ServerName</span></span>
<span data-ttu-id="75a89-116">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="75a89-116">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="75a89-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="75a89-117">-Confirm</span></span>
<span data-ttu-id="75a89-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75a89-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75a89-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75a89-119">-WhatIf</span></span>
<span data-ttu-id="75a89-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75a89-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75a89-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75a89-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75a89-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a89-122">-DefaultProfile</span></span>
<span data-ttu-id="75a89-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="75a89-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a89-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a89-124">CommonParameters</span></span>
<span data-ttu-id="75a89-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75a89-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a89-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75a89-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a89-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75a89-127">INPUTS</span></span>

### <span data-ttu-id="75a89-128">System. String</span><span class="sxs-lookup"><span data-stu-id="75a89-128">System.String</span></span>

## <span data-ttu-id="75a89-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75a89-129">OUTPUTS</span></span>

### <span data-ttu-id="75a89-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="75a89-130">System.Object</span></span>

## <span data-ttu-id="75a89-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="75a89-131">NOTES</span></span>

## <span data-ttu-id="75a89-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75a89-132">RELATED LINKS</span></span>

[<span data-ttu-id="75a89-133">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="75a89-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
