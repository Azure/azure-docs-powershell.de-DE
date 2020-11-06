---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7642F18A-B193-4849-BE3C-1B85FBD213F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: e76ba16f9578eefdce36a1f3d726e027be2a9ed6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504262"
---
# <span data-ttu-id="c5206-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="c5206-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="c5206-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5206-102">SYNOPSIS</span></span>
<span data-ttu-id="c5206-103">Legt einen langfristigen Aufbewahrungs Tresor für Server fest.</span><span class="sxs-lookup"><span data-stu-id="c5206-103">Sets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5206-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5206-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerBackupLongTermRetentionVault -ResourceId <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5206-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5206-105">DESCRIPTION</span></span>
<span data-ttu-id="c5206-106">Das Cmdlet " **Set-AzureRmSqlServerBackupLongTermRetentionVault** " legt das auf diesem Server registrierte Langzeit-Aufbewahrungs Depot fest.</span><span class="sxs-lookup"><span data-stu-id="c5206-106">The **Set-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet sets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="c5206-107">Bei Vault handelt es sich um eine Azure-Sicherungs Ressource, die zum Speichern von Sicherungsdaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c5206-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="c5206-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5206-108">EXAMPLES</span></span>

## <span data-ttu-id="c5206-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5206-109">PARAMETERS</span></span>

### <span data-ttu-id="c5206-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5206-110">-DefaultProfile</span></span>
<span data-ttu-id="c5206-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c5206-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5206-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5206-112">-ResourceGroupName</span></span>
<span data-ttu-id="c5206-113">Gibt den Namen der Ressourcengruppe an, die den Server enthält.</span><span class="sxs-lookup"><span data-stu-id="c5206-113">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="c5206-114">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c5206-114">-ResourceId</span></span>
<span data-ttu-id="c5206-115">Gibt die ID einer Ressource an.</span><span class="sxs-lookup"><span data-stu-id="c5206-115">Specifies the ID of a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5206-116">-Servername</span><span class="sxs-lookup"><span data-stu-id="c5206-116">-ServerName</span></span>
<span data-ttu-id="c5206-117">Gibt den Server an, für den dieses Cmdlet einen Tresor festlegt.</span><span class="sxs-lookup"><span data-stu-id="c5206-117">Specifies the server for which this cmdlet sets a vault.</span></span>

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

### <span data-ttu-id="c5206-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c5206-118">-Confirm</span></span>
<span data-ttu-id="c5206-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c5206-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5206-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5206-120">-WhatIf</span></span>
<span data-ttu-id="c5206-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c5206-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5206-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c5206-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5206-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5206-123">CommonParameters</span></span>
<span data-ttu-id="c5206-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5206-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5206-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5206-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5206-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5206-126">INPUTS</span></span>

### <span data-ttu-id="c5206-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c5206-127">System.String</span></span>

## <span data-ttu-id="c5206-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5206-128">OUTPUTS</span></span>

### <span data-ttu-id="c5206-129">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlServerBackupLongTermRetentionVaultModel</span><span class="sxs-lookup"><span data-stu-id="c5206-129">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlServerBackupLongTermRetentionVaultModel</span></span>

## <span data-ttu-id="c5206-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5206-130">NOTES</span></span>

## <span data-ttu-id="c5206-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5206-131">RELATED LINKS</span></span>

[<span data-ttu-id="c5206-132">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="c5206-132">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Get-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="c5206-133">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="c5206-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
