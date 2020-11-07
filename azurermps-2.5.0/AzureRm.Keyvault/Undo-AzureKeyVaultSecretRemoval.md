---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultsecretremoval
schema: 2.0.0
ms.openlocfilehash: a025dc40a666f643a3e7e232a22451e73f3e60bf
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849287"
---
# <span data-ttu-id="40d48-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="40d48-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="40d48-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="40d48-102">SYNOPSIS</span></span>
<span data-ttu-id="40d48-103">Stellt ein gelöschtes Geheimnis in einem schlüsseltresor in einen aktiven Zustand.</span><span class="sxs-lookup"><span data-stu-id="40d48-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40d48-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="40d48-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40d48-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40d48-105">DESCRIPTION</span></span>
<span data-ttu-id="40d48-106">Mit dem Cmdlet **"Undo-AzureKeyVaultSecretRemoval"** wird ein zuvor gelöschter Schlüssel wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="40d48-106">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="40d48-107">Der wiederhergestellte Schlüssel ist aktiv und kann für alle normalen geheimen Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40d48-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="40d48-108">Der Aufrufer muss über die Berechtigung "Wiederherstellen" verfügen, um diesen Vorgang ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="40d48-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="40d48-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40d48-109">EXAMPLES</span></span>

### <span data-ttu-id="40d48-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="40d48-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="40d48-111">Mit diesem Befehl wird der zuvor gelöschte Geheimtipp "MySecret" in einen aktiven und nutzbaren Zustand zurückgestellt.</span><span class="sxs-lookup"><span data-stu-id="40d48-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="40d48-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="40d48-112">PARAMETERS</span></span>

### <span data-ttu-id="40d48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d48-113">-DefaultProfile</span></span>
<span data-ttu-id="40d48-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="40d48-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40d48-115">-Name</span><span class="sxs-lookup"><span data-stu-id="40d48-115">-Name</span></span>
<span data-ttu-id="40d48-116">Geheimer Name.</span><span class="sxs-lookup"><span data-stu-id="40d48-116">Secret name.</span></span>
<span data-ttu-id="40d48-117">Cmdlet erstellt den FQDN eines geheimen Schlüssels aus Vault-Name, aktuell ausgewählter Umgebung und geheimem Namen.</span><span class="sxs-lookup"><span data-stu-id="40d48-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d48-118">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="40d48-118">-VaultName</span></span>
<span data-ttu-id="40d48-119">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="40d48-119">Vault name.</span></span>
<span data-ttu-id="40d48-120">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="40d48-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="40d48-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="40d48-121">-Confirm</span></span>
<span data-ttu-id="40d48-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="40d48-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40d48-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40d48-123">-WhatIf</span></span>
<span data-ttu-id="40d48-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40d48-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40d48-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="40d48-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40d48-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d48-126">CommonParameters</span></span>
<span data-ttu-id="40d48-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40d48-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d48-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40d48-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d48-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="40d48-129">INPUTS</span></span>

### <span data-ttu-id="40d48-130">System. String</span><span class="sxs-lookup"><span data-stu-id="40d48-130">System.String</span></span>

## <span data-ttu-id="40d48-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="40d48-131">OUTPUTS</span></span>

### <span data-ttu-id="40d48-132">Microsoft. Azure. Commands. keyvault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="40d48-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="40d48-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="40d48-133">NOTES</span></span>

## <span data-ttu-id="40d48-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="40d48-134">RELATED LINKS</span></span>

[<span data-ttu-id="40d48-135">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="40d48-135">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)



[<span data-ttu-id="40d48-136">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="40d48-136">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
