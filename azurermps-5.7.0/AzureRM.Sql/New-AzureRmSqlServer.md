---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
ms.openlocfilehash: 6b9fa4c7fff426f9af19484c7576b9dee341a82e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663036"
---
# <span data-ttu-id="8da30-101">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="8da30-101">New-AzureRmSqlServer</span></span>

## <span data-ttu-id="8da30-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8da30-102">SYNOPSIS</span></span>
<span data-ttu-id="8da30-103">Erstellt einen SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="8da30-103">Creates a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8da30-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8da30-104">SYNTAX</span></span>

```
New-AzureRmSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8da30-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8da30-105">DESCRIPTION</span></span>
<span data-ttu-id="8da30-106">Das Cmdlet **New-AzureRmSqlServer** erstellt einen Azure SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="8da30-106">The **New-AzureRmSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="8da30-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8da30-107">EXAMPLES</span></span>

### <span data-ttu-id="8da30-108">Beispiel 1: Erstellen eines neuen Azure SQL-Datenbankservers</span><span class="sxs-lookup"><span data-stu-id="8da30-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="8da30-109">Dieser Befehl erstellt einen Azure SQL-Datenbankserver der Version 12.</span><span class="sxs-lookup"><span data-stu-id="8da30-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="8da30-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8da30-110">PARAMETERS</span></span>

### <span data-ttu-id="8da30-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8da30-111">-AsJob</span></span>
<span data-ttu-id="8da30-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8da30-112">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da30-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="8da30-113">-AssignIdentity</span></span>
<span data-ttu-id="8da30-114">Sie können eine Azure Active Directory-Identität für diesen Server für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault generieren und zuweisen.</span><span class="sxs-lookup"><span data-stu-id="8da30-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da30-115">-DefaultProfile</span></span>
<span data-ttu-id="8da30-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8da30-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da30-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="8da30-117">-Location</span></span>
<span data-ttu-id="8da30-118">Gibt den Speicherort des Rechenzentrums an, in dem dieses Cmdlet den Server erstellt.</span><span class="sxs-lookup"><span data-stu-id="8da30-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da30-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8da30-119">-ResourceGroupName</span></span>
<span data-ttu-id="8da30-120">Gibt den Namen der Ressourcengruppe an, der das Cmdlet den Server zuweist.</span><span class="sxs-lookup"><span data-stu-id="8da30-120">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="8da30-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="8da30-121">-ServerName</span></span>
<span data-ttu-id="8da30-122">Gibt den Namen des neuen Servers an.</span><span class="sxs-lookup"><span data-stu-id="8da30-122">Specifies the name of the new server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da30-123">-Server Version vom</span><span class="sxs-lookup"><span data-stu-id="8da30-123">-ServerVersion</span></span>
<span data-ttu-id="8da30-124">Gibt die Version des neuen Servers an.</span><span class="sxs-lookup"><span data-stu-id="8da30-124">Specifies the version of the new server.</span></span> <span data-ttu-id="8da30-125">Die zulässigen Werte für diesen Parameter lauten: 2,0 und 12,0.</span><span class="sxs-lookup"><span data-stu-id="8da30-125">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

<span data-ttu-id="8da30-126">Geben Sie 2,0 an, um einen Server der Version 11 zu erstellen, oder 12,0, um einen Server der Version 12 zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8da30-126">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da30-127">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="8da30-127">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="8da30-128">Gibt die SQL-Datenbankserver-Administratoranmeldeinformationen für den neuen Server an.</span><span class="sxs-lookup"><span data-stu-id="8da30-128">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="8da30-129">Verwenden Sie das Get-Credential-Cmdlet, um ein **PSCredential** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8da30-129">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="8da30-130">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="8da30-130">For more information, type `Get-Help
Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da30-131">-Tags</span><span class="sxs-lookup"><span data-stu-id="8da30-131">-Tags</span></span>
<span data-ttu-id="8da30-132">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="8da30-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8da30-133">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8da30-133">For example:</span></span>

<span data-ttu-id="8da30-134">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="8da30-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da30-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8da30-135">-Confirm</span></span>
<span data-ttu-id="8da30-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8da30-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da30-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8da30-137">-WhatIf</span></span>
<span data-ttu-id="8da30-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8da30-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8da30-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8da30-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da30-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da30-140">CommonParameters</span></span>
<span data-ttu-id="8da30-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8da30-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da30-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8da30-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da30-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8da30-143">INPUTS</span></span>

### <span data-ttu-id="8da30-144">Keine</span><span class="sxs-lookup"><span data-stu-id="8da30-144">None</span></span>
<span data-ttu-id="8da30-145">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8da30-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8da30-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8da30-146">OUTPUTS</span></span>

### <span data-ttu-id="8da30-147">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="8da30-147">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="8da30-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="8da30-148">NOTES</span></span>

## <span data-ttu-id="8da30-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8da30-149">RELATED LINKS</span></span>

[<span data-ttu-id="8da30-150">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="8da30-150">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="8da30-151">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="8da30-151">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="8da30-152">Satz-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="8da30-152">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="8da30-153">Neu – AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8da30-153">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="8da30-154">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="8da30-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
